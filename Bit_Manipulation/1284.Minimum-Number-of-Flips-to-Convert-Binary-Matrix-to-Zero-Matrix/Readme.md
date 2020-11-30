### 1284.Minimum-Number-of-Flips-to-Convert-Binary-Matrix-to-Zero-Matrix

首先我们应该有这样一个认识，每个元素最多只需要flip一次，flip两次及以上都是没有意义的操作。再考虑到矩阵的维度非常小（不超过3x3），因此即使穷举每个元素是否flip，最多只有2^9种不同的可能性。对于每种可能性，我们最多再花o(4mn)的时间来验证是否能实现矩阵全部翻零。因此这种暴力的方法的时间复杂度是可以接受的。

如果还想优化一点的话，可以用Gosper's hack，按照“1-bit的个数”从小到大地枚举状态。一旦发现可以实现矩阵翻零，即可输出答案。