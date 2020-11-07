---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A0D620DA-B5A3-4F8F-BD43-A58630C95432
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchComputeNodeUser.md
ms.openlocfilehash: ddf0632be8ea7749b733d21beecfdb539272d6c3
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2020
ms.locfileid: "93968695"
---
# <span data-ttu-id="88d25-101">Set-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="88d25-101">Set-AzBatchComputeNodeUser</span></span>

## <span data-ttu-id="88d25-102">摘要</span><span class="sxs-lookup"><span data-stu-id="88d25-102">SYNOPSIS</span></span>
<span data-ttu-id="88d25-103">在批次計算節點上修改帳戶的屬性。</span><span class="sxs-lookup"><span data-stu-id="88d25-103">Modifies properties of an account on a Batch compute node.</span></span>

## <span data-ttu-id="88d25-104">句法</span><span class="sxs-lookup"><span data-stu-id="88d25-104">SYNTAX</span></span>

```
Set-AzBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 [-Password] <SecureString> [-ExpiryTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88d25-105">說明</span><span class="sxs-lookup"><span data-stu-id="88d25-105">DESCRIPTION</span></span>
<span data-ttu-id="88d25-106">**AzBatchComputeNodeUser** Cmdlet 會修改 Azure Batch 計算節點上使用者帳戶的屬性。</span><span class="sxs-lookup"><span data-stu-id="88d25-106">The **Set-AzBatchComputeNodeUser** cmdlet modifies properties of a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="88d25-107">示例</span><span class="sxs-lookup"><span data-stu-id="88d25-107">EXAMPLES</span></span>

### <span data-ttu-id="88d25-108">範例1：更新使用者帳戶</span><span class="sxs-lookup"><span data-stu-id="88d25-108">Example 1: Update a user account</span></span>
```
PS C:\>Set-AzBatchComputeNodeUser -PoolId "ContosoPool" -ComputeNodeId "tvm-3257026573_1-20150904t230807z" -Name "PFuller" -BatchContext $Context -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(14))
```

<span data-ttu-id="88d25-109">這個命令會修改在名為 ContosoPool 的 pool 中擁有指定 ID 的 compute 節點上名為 PFuller 的使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="88d25-109">This command modifies user account named PFuller on the compute node that has the specified ID in the pool named ContosoPool.</span></span>
<span data-ttu-id="88d25-110">此命令會變更帳戶密碼及到期時間。</span><span class="sxs-lookup"><span data-stu-id="88d25-110">The command changes the account password and expiry time.</span></span>

## <span data-ttu-id="88d25-111">參數</span><span class="sxs-lookup"><span data-stu-id="88d25-111">PARAMETERS</span></span>

### <span data-ttu-id="88d25-112">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="88d25-112">-BatchContext</span></span>
<span data-ttu-id="88d25-113">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="88d25-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="88d25-114">如果您使用 Get-AzBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="88d25-114">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="88d25-115">若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="88d25-115">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="88d25-116">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="88d25-116">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="88d25-117">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="88d25-117">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="88d25-118">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="88d25-118">-ComputeNodeId</span></span>
<span data-ttu-id="88d25-119">指定此 Cmdlet 在其上執行的計算節點的識別碼。</span><span class="sxs-lookup"><span data-stu-id="88d25-119">Specifies the ID of the compute node on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="88d25-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88d25-120">-DefaultProfile</span></span>
<span data-ttu-id="88d25-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="88d25-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88d25-122">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="88d25-122">-ExpiryTime</span></span>
<span data-ttu-id="88d25-123">指定使用者帳戶的到期時間。</span><span class="sxs-lookup"><span data-stu-id="88d25-123">Specifies the expiry time for the user account.</span></span>

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

### <span data-ttu-id="88d25-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="88d25-124">-Name</span></span>
<span data-ttu-id="88d25-125">指定此 Cmdlet 修改的使用者帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="88d25-125">Specifies the name of the user account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="88d25-126">-Password</span><span class="sxs-lookup"><span data-stu-id="88d25-126">-Password</span></span>
<span data-ttu-id="88d25-127">指定使用者帳戶的密碼。</span><span class="sxs-lookup"><span data-stu-id="88d25-127">Specifies the password for the user account.</span></span>

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

### <span data-ttu-id="88d25-128">-PoolId</span><span class="sxs-lookup"><span data-stu-id="88d25-128">-PoolId</span></span>
<span data-ttu-id="88d25-129">指定包含此 Cmdlet 操作之計算節點之池的 ID。</span><span class="sxs-lookup"><span data-stu-id="88d25-129">Specifies the ID of the pool that contains the compute node on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="88d25-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88d25-130">CommonParameters</span></span>
<span data-ttu-id="88d25-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="88d25-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88d25-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="88d25-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88d25-133">輸入</span><span class="sxs-lookup"><span data-stu-id="88d25-133">INPUTS</span></span>

### <span data-ttu-id="88d25-134">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="88d25-134">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="88d25-135">輸出</span><span class="sxs-lookup"><span data-stu-id="88d25-135">OUTPUTS</span></span>

### <span data-ttu-id="88d25-136">System.void</span><span class="sxs-lookup"><span data-stu-id="88d25-136">System.Void</span></span>

## <span data-ttu-id="88d25-137">筆記</span><span class="sxs-lookup"><span data-stu-id="88d25-137">NOTES</span></span>

## <span data-ttu-id="88d25-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="88d25-138">RELATED LINKS</span></span>

[<span data-ttu-id="88d25-139">AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="88d25-139">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="88d25-140">新-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="88d25-140">New-AzBatchComputeNodeUser</span></span>](./New-AzBatchComputeNodeUser.md)

[<span data-ttu-id="88d25-141">移除-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="88d25-141">Remove-AzBatchComputeNodeUser</span></span>](./Remove-AzBatchComputeNodeUser.md)

[<span data-ttu-id="88d25-142">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="88d25-142">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


