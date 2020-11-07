---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: A0D620DA-B5A3-4F8F-BD43-A58630C95432
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchComputeNodeUser.md
ms.openlocfilehash: 6fb398e44b2e6de8a0d00e9a8d737916fafa2472
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626167"
---
# <span data-ttu-id="b5542-101">Set-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="b5542-101">Set-AzureBatchComputeNodeUser</span></span>

## <span data-ttu-id="b5542-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b5542-102">SYNOPSIS</span></span>
<span data-ttu-id="b5542-103">在批次計算節點上修改帳戶的屬性。</span><span class="sxs-lookup"><span data-stu-id="b5542-103">Modifies properties of an account on a Batch compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5542-104">句法</span><span class="sxs-lookup"><span data-stu-id="b5542-104">SYNTAX</span></span>

```
Set-AzureBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 [-Password] <SecureString> [-ExpiryTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5542-105">說明</span><span class="sxs-lookup"><span data-stu-id="b5542-105">DESCRIPTION</span></span>
<span data-ttu-id="b5542-106">**AzureBatchComputeNodeUser** Cmdlet 會修改 Azure Batch 計算節點上使用者帳戶的屬性。</span><span class="sxs-lookup"><span data-stu-id="b5542-106">The **Set-AzureBatchComputeNodeUser** cmdlet modifies properties of a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="b5542-107">示例</span><span class="sxs-lookup"><span data-stu-id="b5542-107">EXAMPLES</span></span>

### <span data-ttu-id="b5542-108">範例1：更新使用者帳戶</span><span class="sxs-lookup"><span data-stu-id="b5542-108">Example 1: Update a user account</span></span>
```
PS C:\>Set-AzureBatchComputeNodeUser -PoolId "ContosoPool" -ComputeNodeId "tvm-3257026573_1-20150904t230807z" -Name "PFuller" -BatchContext $Context -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(14))
```

<span data-ttu-id="b5542-109">這個命令會修改在名為 ContosoPool 的 pool 中擁有指定 ID 的 compute 節點上名為 PFuller 的使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="b5542-109">This command modifies user account named PFuller on the compute node that has the specified ID in the pool named ContosoPool.</span></span>
<span data-ttu-id="b5542-110">此命令會變更帳戶密碼及到期時間。</span><span class="sxs-lookup"><span data-stu-id="b5542-110">The command changes the account password and expiry time.</span></span>

## <span data-ttu-id="b5542-111">參數</span><span class="sxs-lookup"><span data-stu-id="b5542-111">PARAMETERS</span></span>

### <span data-ttu-id="b5542-112">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="b5542-112">-BatchContext</span></span>
<span data-ttu-id="b5542-113">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="b5542-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b5542-114">如果您使用 Get-AzureRmBatchAccount Cmdlet 來取得您的 BatchAccountCoNtext，則在與批次服務互動時，將會使用 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="b5542-114">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="b5542-115">若要改為使用共用金鑰驗證，請使用 Get-AzureRmBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。</span><span class="sxs-lookup"><span data-stu-id="b5542-115">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="b5542-116">使用共用金鑰驗證時，預設會使用主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="b5542-116">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="b5542-117">若要變更要使用的索引鍵，請設定 BatchAccountCoNtext 屬性。</span><span class="sxs-lookup"><span data-stu-id="b5542-117">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5542-118">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="b5542-118">-ComputeNodeId</span></span>
<span data-ttu-id="b5542-119">指定此 Cmdlet 在其上執行的計算節點的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b5542-119">Specifies the ID of the compute node on which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5542-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5542-120">-DefaultProfile</span></span>
<span data-ttu-id="b5542-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b5542-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5542-122">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="b5542-122">-ExpiryTime</span></span>
<span data-ttu-id="b5542-123">指定使用者帳戶的到期時間。</span><span class="sxs-lookup"><span data-stu-id="b5542-123">Specifies the expiry time for the user account.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5542-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="b5542-124">-Name</span></span>
<span data-ttu-id="b5542-125">指定此 Cmdlet 修改的使用者帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="b5542-125">Specifies the name of the user account that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5542-126">-Password</span><span class="sxs-lookup"><span data-stu-id="b5542-126">-Password</span></span>
<span data-ttu-id="b5542-127">指定使用者帳戶的密碼。</span><span class="sxs-lookup"><span data-stu-id="b5542-127">Specifies the password for the user account.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5542-128">-PoolId</span><span class="sxs-lookup"><span data-stu-id="b5542-128">-PoolId</span></span>
<span data-ttu-id="b5542-129">指定包含此 Cmdlet 操作之計算節點之池的 ID。</span><span class="sxs-lookup"><span data-stu-id="b5542-129">Specifies the ID of the pool that contains the compute node on which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5542-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5542-130">CommonParameters</span></span>
<span data-ttu-id="b5542-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b5542-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5542-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b5542-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5542-133">輸入</span><span class="sxs-lookup"><span data-stu-id="b5542-133">INPUTS</span></span>

### <span data-ttu-id="b5542-134">BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="b5542-134">BatchAccountContext</span></span>
<span data-ttu-id="b5542-135">形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="b5542-135">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="b5542-136">輸出</span><span class="sxs-lookup"><span data-stu-id="b5542-136">OUTPUTS</span></span>

## <span data-ttu-id="b5542-137">筆記</span><span class="sxs-lookup"><span data-stu-id="b5542-137">NOTES</span></span>

## <span data-ttu-id="b5542-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="b5542-138">RELATED LINKS</span></span>

[<span data-ttu-id="b5542-139">AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="b5542-139">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="b5542-140">新-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="b5542-140">New-AzureBatchComputeNodeUser</span></span>](./New-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="b5542-141">移除-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="b5542-141">Remove-AzureBatchComputeNodeUser</span></span>](./Remove-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="b5542-142">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b5542-142">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


