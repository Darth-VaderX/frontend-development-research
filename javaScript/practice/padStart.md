String.prototype.padStart = function (targetLength, padString) {
  targetLength = Number(targetLength) || 0;
  padString = String(padString || ' ');

  if (this.length >= targetLength) {
    return this;
  }

  let result = '';

  while (result.length < targetLength - this.length) {
    result += padString;
  }

  return result.slice(0, targetLength - this.length) + this;
};
