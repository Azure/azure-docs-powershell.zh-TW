---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 818D5D85-B6D5-458C-A26E-E4DE8E111A10
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchAccount.md
ms.openlocfilehash: 33ada04a3e45c1c8cc9768ef9da98abe781aa01a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903678"
---
# <span data-ttu-id="71cce-101">Get-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="71cce-101">Get-AzBatchAccount</span></span>

## <span data-ttu-id="71cce-102">簡介</span><span class="sxs-lookup"><span data-stu-id="71cce-102">SYNOPSIS</span></span>
<span data-ttu-id="71cce-103">在目前的訂閱中，獲得批次帳戶。</span><span class="sxs-lookup"><span data-stu-id="71cce-103">Gets a Batch account in the current subscription.</span></span>

## <span data-ttu-id="71cce-104">語法</span><span class="sxs-lookup"><span data-stu-id="71cce-104">SYNTAX</span></span>

```
Get-AzBatchAccount [[-AccountName] <String>] [[-ResourceGroupName] <String>] [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71cce-105">描述</span><span class="sxs-lookup"><span data-stu-id="71cce-105">DESCRIPTION</span></span>
<span data-ttu-id="71cce-106">**Get-AzBatchAccount** Cmdlet 會取得目前訂閱中的 Azure Batch 帳戶。</span><span class="sxs-lookup"><span data-stu-id="71cce-106">The **Get-AzBatchAccount** cmdlet gets an Azure Batch account in the current subscription.</span></span> <span data-ttu-id="71cce-107">您可以使用 *AccountName* 參數取得單一帳戶，或使用 *ResourceGroupName* 參數取得該資源群組下的帳戶。</span><span class="sxs-lookup"><span data-stu-id="71cce-107">You can use the *AccountName* parameter to get a single account, or you can use the *ResourceGroupName* parameter to get accounts under that resource group.</span></span>

## <span data-ttu-id="71cce-108">例子</span><span class="sxs-lookup"><span data-stu-id="71cce-108">EXAMPLES</span></span>

### <span data-ttu-id="71cce-109">範例 1：根據名稱取得批次帳戶</span><span class="sxs-lookup"><span data-stu-id="71cce-109">Example 1: Get a batch account by name</span></span>
```
PS C:\>Get-AzBatchAccount -AccountName "pfuller"
AccountName                  : pfuller
Location                     : westus
ResourceGroupName            : CmdletExampleRG
DedicatedCoreQuota           : 20
LowPriorityCoreQuota         : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://pfuller.westus.batch.azure.com
```

<span data-ttu-id="71cce-110">此命令會獲得名為 pfuller 的批次帳戶。</span><span class="sxs-lookup"><span data-stu-id="71cce-110">This command gets the batch account named pfuller.</span></span>

### <span data-ttu-id="71cce-111">範例 2：取得與資源群組相關聯的批次帳戶</span><span class="sxs-lookup"><span data-stu-id="71cce-111">Example 2: Get the batch accounts associated with a resource group</span></span>
```
PS C:\>Get-AzBatchAccount -ResourceGroupName "CmdletExampleRG"
AccountName                  : cmdletexample
Location                     : westus
ResourceGroupName            : CmdletExampleRG
DedicatedCoreQuota           : 20
LowPriorityCoreQuota         : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
AccountName                  : cmdletexample2
Location                     : westus
ResourceGroupName            : CmdletExampleRG
DedicatedCoreQuota           : 20
LowPriorityCoreQuota         : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="71cce-112">此命令會獲得與 CmdletExampleRG 資源群組相關聯的批次處理帳戶。</span><span class="sxs-lookup"><span data-stu-id="71cce-112">This command gets the batch accounts associated with the CmdletExampleRG resource group.</span></span>

## <span data-ttu-id="71cce-113">參數</span><span class="sxs-lookup"><span data-stu-id="71cce-113">PARAMETERS</span></span>

### <span data-ttu-id="71cce-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="71cce-114">-AccountName</span></span>
<span data-ttu-id="71cce-115">指定帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="71cce-115">Specifies the name of an account.</span></span>
<span data-ttu-id="71cce-116">如果您指定帳戶名稱，此 Cmdlet 只會返回該帳戶。</span><span class="sxs-lookup"><span data-stu-id="71cce-116">If you specify an account name, this cmdlet only returns that account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71cce-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71cce-117">-DefaultProfile</span></span>
<span data-ttu-id="71cce-118">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="71cce-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71cce-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71cce-119">-ResourceGroupName</span></span>
<span data-ttu-id="71cce-120">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="71cce-120">Specifies the name of a resource group.</span></span>
<span data-ttu-id="71cce-121">如果您指定資源群組，此 Cmdlet 會獲得指定資源群組下的帳戶。</span><span class="sxs-lookup"><span data-stu-id="71cce-121">If you specify a resource group, this cmdlet gets the accounts under the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71cce-122">-標記</span><span class="sxs-lookup"><span data-stu-id="71cce-122">-Tag</span></span>
<span data-ttu-id="71cce-123">以雜湊表格形式建立索引鍵值組。</span><span class="sxs-lookup"><span data-stu-id="71cce-123">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="71cce-124">例如：@{key0="value0";key1=$null;key2="value2"} 此 Cmdlet 會獲得包含此參數指定之標籤的帳戶。</span><span class="sxs-lookup"><span data-stu-id="71cce-124">For example: @{key0="value0";key1=$null;key2="value2"} This cmdlet gets accounts that contain the tags that this parameter specifies.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71cce-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71cce-125">CommonParameters</span></span>
<span data-ttu-id="71cce-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="71cce-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71cce-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="71cce-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71cce-128">輸入</span><span class="sxs-lookup"><span data-stu-id="71cce-128">INPUTS</span></span>

### <span data-ttu-id="71cce-129">System.String</span><span class="sxs-lookup"><span data-stu-id="71cce-129">System.String</span></span>

### <span data-ttu-id="71cce-130">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="71cce-130">System.Collections.Hashtable</span></span>

## <span data-ttu-id="71cce-131">輸出</span><span class="sxs-lookup"><span data-stu-id="71cce-131">OUTPUTS</span></span>

### <span data-ttu-id="71cce-132">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="71cce-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="71cce-133">筆記</span><span class="sxs-lookup"><span data-stu-id="71cce-133">NOTES</span></span>

## <span data-ttu-id="71cce-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="71cce-134">RELATED LINKS</span></span>

[<span data-ttu-id="71cce-135">New-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="71cce-135">New-AzBatchAccount</span></span>](./New-AzBatchAccount.md)

[<span data-ttu-id="71cce-136">Remove-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="71cce-136">Remove-AzBatchAccount</span></span>](./Remove-AzBatchAccount.md)

[<span data-ttu-id="71cce-137">Set-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="71cce-137">Set-AzBatchAccount</span></span>](./Set-AzBatchAccount.md)

[<span data-ttu-id="71cce-138">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="71cce-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
