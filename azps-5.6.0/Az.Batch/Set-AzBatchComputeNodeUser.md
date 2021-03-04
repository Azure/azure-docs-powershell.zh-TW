---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A0D620DA-B5A3-4F8F-BD43-A58630C95432
online version: https://docs.microsoft.com/powershell/module/az.batch/set-azbatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchComputeNodeUser.md
ms.openlocfilehash: c76c10d282d7a2b50cf0b35793cdda080d944740
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915610"
---
# <span data-ttu-id="76b76-101">Set-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="76b76-101">Set-AzBatchComputeNodeUser</span></span>

## <span data-ttu-id="76b76-102">簡介</span><span class="sxs-lookup"><span data-stu-id="76b76-102">SYNOPSIS</span></span>
<span data-ttu-id="76b76-103">修改 Batch 計算節點上帳戶的屬性。</span><span class="sxs-lookup"><span data-stu-id="76b76-103">Modifies properties of an account on a Batch compute node.</span></span>

## <span data-ttu-id="76b76-104">語法</span><span class="sxs-lookup"><span data-stu-id="76b76-104">SYNTAX</span></span>

```
Set-AzBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 [-Password] <SecureString> [-ExpiryTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76b76-105">描述</span><span class="sxs-lookup"><span data-stu-id="76b76-105">DESCRIPTION</span></span>
<span data-ttu-id="76b76-106">**Set-AzBatchComputeNodeUser** Cmdlet 會修改 Azure Batch 計算節點上使用者帳戶的屬性。</span><span class="sxs-lookup"><span data-stu-id="76b76-106">The **Set-AzBatchComputeNodeUser** cmdlet modifies properties of a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="76b76-107">例子</span><span class="sxs-lookup"><span data-stu-id="76b76-107">EXAMPLES</span></span>

### <span data-ttu-id="76b76-108">範例 1：更新使用者帳戶</span><span class="sxs-lookup"><span data-stu-id="76b76-108">Example 1: Update a user account</span></span>
```
PS C:\>Set-AzBatchComputeNodeUser -PoolId "ContosoPool" -ComputeNodeId "tvm-3257026573_1-20150904t230807z" -Name "PFuller" -BatchContext $Context -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(14))
```

<span data-ttu-id="76b76-109">此命令會修改計算節點上名為 PFuller 的使用者帳戶，該帳戶在名為 ContosoPool 的集中具有指定識別碼。</span><span class="sxs-lookup"><span data-stu-id="76b76-109">This command modifies user account named PFuller on the compute node that has the specified ID in the pool named ContosoPool.</span></span>
<span data-ttu-id="76b76-110">命令會變更帳戶密碼和到期日。</span><span class="sxs-lookup"><span data-stu-id="76b76-110">The command changes the account password and expiry time.</span></span>

## <span data-ttu-id="76b76-111">參數</span><span class="sxs-lookup"><span data-stu-id="76b76-111">PARAMETERS</span></span>

### <span data-ttu-id="76b76-112">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="76b76-112">-BatchContext</span></span>
<span data-ttu-id="76b76-113">指定此 Cmdlet 用來與批次處理服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="76b76-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="76b76-114">如果您使用 Get-AzBatchAccount Cmdlet 取得 BatchAccountCoNtext，則與批次處理服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="76b76-114">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="76b76-115">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 取得已填入便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="76b76-115">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="76b76-116">使用共用金鑰驗證時，預設會使用主便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="76b76-116">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="76b76-117">若要變更使用的金鑰，請設定 BatchAccountCoNtext.KeyInUse 屬性。</span><span class="sxs-lookup"><span data-stu-id="76b76-117">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76b76-118">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="76b76-118">-ComputeNodeId</span></span>
<span data-ttu-id="76b76-119">指定此 Cmdlet 操作之計算節點的識別碼。</span><span class="sxs-lookup"><span data-stu-id="76b76-119">Specifies the ID of the compute node on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76b76-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76b76-120">-DefaultProfile</span></span>
<span data-ttu-id="76b76-121">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="76b76-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76b76-122">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="76b76-122">-ExpiryTime</span></span>
<span data-ttu-id="76b76-123">指定使用者帳戶的到期時間。</span><span class="sxs-lookup"><span data-stu-id="76b76-123">Specifies the expiry time for the user account.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76b76-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="76b76-124">-Name</span></span>
<span data-ttu-id="76b76-125">指定此 Cmdlet 修改的使用者帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="76b76-125">Specifies the name of the user account that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76b76-126">-密碼</span><span class="sxs-lookup"><span data-stu-id="76b76-126">-Password</span></span>
<span data-ttu-id="76b76-127">指定使用者帳戶的密碼。</span><span class="sxs-lookup"><span data-stu-id="76b76-127">Specifies the password for the user account.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76b76-128">-PoolId</span><span class="sxs-lookup"><span data-stu-id="76b76-128">-PoolId</span></span>
<span data-ttu-id="76b76-129">指定包含此 Cmdlet 操作之計算節點之資料庫的識別碼。</span><span class="sxs-lookup"><span data-stu-id="76b76-129">Specifies the ID of the pool that contains the compute node on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76b76-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76b76-130">CommonParameters</span></span>
<span data-ttu-id="76b76-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="76b76-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76b76-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="76b76-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76b76-133">輸入</span><span class="sxs-lookup"><span data-stu-id="76b76-133">INPUTS</span></span>

### <span data-ttu-id="76b76-134">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="76b76-134">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="76b76-135">輸出</span><span class="sxs-lookup"><span data-stu-id="76b76-135">OUTPUTS</span></span>

### <span data-ttu-id="76b76-136">System.Void</span><span class="sxs-lookup"><span data-stu-id="76b76-136">System.Void</span></span>

## <span data-ttu-id="76b76-137">筆記</span><span class="sxs-lookup"><span data-stu-id="76b76-137">NOTES</span></span>

## <span data-ttu-id="76b76-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="76b76-138">RELATED LINKS</span></span>

[<span data-ttu-id="76b76-139">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="76b76-139">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="76b76-140">New-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="76b76-140">New-AzBatchComputeNodeUser</span></span>](./New-AzBatchComputeNodeUser.md)

[<span data-ttu-id="76b76-141">Remove-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="76b76-141">Remove-AzBatchComputeNodeUser</span></span>](./Remove-AzBatchComputeNodeUser.md)

[<span data-ttu-id="76b76-142">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="76b76-142">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
