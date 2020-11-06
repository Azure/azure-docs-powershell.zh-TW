---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: A0D620DA-B5A3-4F8F-BD43-A58630C95432
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchComputeNodeUser.md
ms.openlocfilehash: a5e8fd6e6cfba8832365f385cc90357bac59efb0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450016"
---
# <span data-ttu-id="3d21e-101">Set-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="3d21e-101">Set-AzureBatchComputeNodeUser</span></span>

## <span data-ttu-id="3d21e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3d21e-102">SYNOPSIS</span></span>
<span data-ttu-id="3d21e-103">在批次計算節點上修改帳戶的屬性。</span><span class="sxs-lookup"><span data-stu-id="3d21e-103">Modifies properties of an account on a Batch compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d21e-104">句法</span><span class="sxs-lookup"><span data-stu-id="3d21e-104">SYNTAX</span></span>

```
Set-AzureBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 [-Password] <String> [-ExpiryTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d21e-105">說明</span><span class="sxs-lookup"><span data-stu-id="3d21e-105">DESCRIPTION</span></span>
<span data-ttu-id="3d21e-106">**AzureBatchComputeNodeUser** Cmdlet 會修改 Azure Batch 計算節點上使用者帳戶的屬性。</span><span class="sxs-lookup"><span data-stu-id="3d21e-106">The **Set-AzureBatchComputeNodeUser** cmdlet modifies properties of a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="3d21e-107">示例</span><span class="sxs-lookup"><span data-stu-id="3d21e-107">EXAMPLES</span></span>

### <span data-ttu-id="3d21e-108">範例1：更新使用者帳戶</span><span class="sxs-lookup"><span data-stu-id="3d21e-108">Example 1: Update a user account</span></span>
```
PS C:\>Set-AzureBatchComputeNodeUser -PoolId "ContosoPool" -ComputeNodeId "tvm-3257026573_1-20150904t230807z" -Name "PFuller" -BatchContext $Context -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(14))
```

<span data-ttu-id="3d21e-109">這個命令會修改在名為 ContosoPool 的 pool 中擁有指定 ID 的 compute 節點上名為 PFuller 的使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="3d21e-109">This command modifies user account named PFuller on the compute node that has the specified ID in the pool named ContosoPool.</span></span>
<span data-ttu-id="3d21e-110">此命令會變更帳戶密碼及到期時間。</span><span class="sxs-lookup"><span data-stu-id="3d21e-110">The command changes the account password and expiry time.</span></span>

## <span data-ttu-id="3d21e-111">參數</span><span class="sxs-lookup"><span data-stu-id="3d21e-111">PARAMETERS</span></span>

### <span data-ttu-id="3d21e-112">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="3d21e-112">-BatchContext</span></span>
<span data-ttu-id="3d21e-113">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="3d21e-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="3d21e-114">若要取得包含您訂閱之便捷鍵的 **BatchAccountCoNtext** 物件，請使用 Get-AzureRmBatchAccountKeys Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3d21e-114">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="3d21e-115">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="3d21e-115">-ComputeNodeId</span></span>
<span data-ttu-id="3d21e-116">指定此 Cmdlet 在其上執行的計算節點的識別碼。</span><span class="sxs-lookup"><span data-stu-id="3d21e-116">Specifies the ID of the compute node on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="3d21e-117">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="3d21e-117">-ExpiryTime</span></span>
<span data-ttu-id="3d21e-118">指定使用者帳戶的到期時間。</span><span class="sxs-lookup"><span data-stu-id="3d21e-118">Specifies the expiry time for the user account.</span></span>

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

### <span data-ttu-id="3d21e-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="3d21e-119">-Name</span></span>
<span data-ttu-id="3d21e-120">指定此 Cmdlet 修改的使用者帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="3d21e-120">Specifies the name of the user account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="3d21e-121">-Password</span><span class="sxs-lookup"><span data-stu-id="3d21e-121">-Password</span></span>
<span data-ttu-id="3d21e-122">指定使用者帳戶的密碼。</span><span class="sxs-lookup"><span data-stu-id="3d21e-122">Specifies the password for the user account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d21e-123">-PoolId</span><span class="sxs-lookup"><span data-stu-id="3d21e-123">-PoolId</span></span>
<span data-ttu-id="3d21e-124">指定包含此 Cmdlet 操作之計算節點之池的 ID。</span><span class="sxs-lookup"><span data-stu-id="3d21e-124">Specifies the ID of the pool that contains the compute node on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="3d21e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d21e-125">-DefaultProfile</span></span>
<span data-ttu-id="3d21e-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3d21e-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d21e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d21e-127">CommonParameters</span></span>
<span data-ttu-id="3d21e-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3d21e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d21e-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3d21e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d21e-130">輸入</span><span class="sxs-lookup"><span data-stu-id="3d21e-130">INPUTS</span></span>

### <span data-ttu-id="3d21e-131">BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="3d21e-131">BatchAccountContext</span></span>
<span data-ttu-id="3d21e-132">形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="3d21e-132">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="3d21e-133">輸出</span><span class="sxs-lookup"><span data-stu-id="3d21e-133">OUTPUTS</span></span>

## <span data-ttu-id="3d21e-134">筆記</span><span class="sxs-lookup"><span data-stu-id="3d21e-134">NOTES</span></span>

## <span data-ttu-id="3d21e-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="3d21e-135">RELATED LINKS</span></span>

[<span data-ttu-id="3d21e-136">AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="3d21e-136">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="3d21e-137">新-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="3d21e-137">New-AzureBatchComputeNodeUser</span></span>](./New-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="3d21e-138">移除-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="3d21e-138">Remove-AzureBatchComputeNodeUser</span></span>](./Remove-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="3d21e-139">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3d21e-139">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


