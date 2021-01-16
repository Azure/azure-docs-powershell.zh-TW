---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 818D5D85-B6D5-458C-A26E-E4DE8E111A10
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchAccount.md
ms.openlocfilehash: 66bab11ab5632464eed8ee160df527b0e44f053d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98285159"
---
# <span data-ttu-id="a73e2-101">Get-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="a73e2-101">Get-AzBatchAccount</span></span>

## <span data-ttu-id="a73e2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a73e2-102">SYNOPSIS</span></span>
<span data-ttu-id="a73e2-103">取得目前訂閱中的批次帳戶。</span><span class="sxs-lookup"><span data-stu-id="a73e2-103">Gets a Batch account in the current subscription.</span></span>

## <span data-ttu-id="a73e2-104">句法</span><span class="sxs-lookup"><span data-stu-id="a73e2-104">SYNTAX</span></span>

```
Get-AzBatchAccount [[-AccountName] <String>] [[-ResourceGroupName] <String>] [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a73e2-105">說明</span><span class="sxs-lookup"><span data-stu-id="a73e2-105">DESCRIPTION</span></span>
<span data-ttu-id="a73e2-106">**AzBatchAccount** Cmdlet 會在目前的訂閱中取得 Azure Batch 帳戶。</span><span class="sxs-lookup"><span data-stu-id="a73e2-106">The **Get-AzBatchAccount** cmdlet gets an Azure Batch account in the current subscription.</span></span> <span data-ttu-id="a73e2-107">您可以使用 *AccountName* 參數來取得單一帳戶，或者您可以使用 *ResourceGroupName* 參數來取得該資源群組下的帳戶。</span><span class="sxs-lookup"><span data-stu-id="a73e2-107">You can use the *AccountName* parameter to get a single account, or you can use the *ResourceGroupName* parameter to get accounts under that resource group.</span></span>

## <span data-ttu-id="a73e2-108">示例</span><span class="sxs-lookup"><span data-stu-id="a73e2-108">EXAMPLES</span></span>

### <span data-ttu-id="a73e2-109">範例1：透過名稱取得批次帳戶</span><span class="sxs-lookup"><span data-stu-id="a73e2-109">Example 1: Get a batch account by name</span></span>
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

<span data-ttu-id="a73e2-110">這個命令會取得名為 pfuller 的批次帳戶。</span><span class="sxs-lookup"><span data-stu-id="a73e2-110">This command gets the batch account named pfuller.</span></span>

### <span data-ttu-id="a73e2-111">範例2：取得與資源群組相關聯的批次帳戶</span><span class="sxs-lookup"><span data-stu-id="a73e2-111">Example 2: Get the batch accounts associated with a resource group</span></span>
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

<span data-ttu-id="a73e2-112">這個命令會取得與 CmdletExampleRG 資源群組相關聯的批次帳戶。</span><span class="sxs-lookup"><span data-stu-id="a73e2-112">This command gets the batch accounts associated with the CmdletExampleRG resource group.</span></span>

## <span data-ttu-id="a73e2-113">參數</span><span class="sxs-lookup"><span data-stu-id="a73e2-113">PARAMETERS</span></span>

### <span data-ttu-id="a73e2-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a73e2-114">-AccountName</span></span>
<span data-ttu-id="a73e2-115">指定帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="a73e2-115">Specifies the name of an account.</span></span>
<span data-ttu-id="a73e2-116">如果您指定帳戶名稱，這個 Cmdlet 只會傳回該帳戶。</span><span class="sxs-lookup"><span data-stu-id="a73e2-116">If you specify an account name, this cmdlet only returns that account.</span></span>

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

### <span data-ttu-id="a73e2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a73e2-117">-DefaultProfile</span></span>
<span data-ttu-id="a73e2-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a73e2-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a73e2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a73e2-119">-ResourceGroupName</span></span>
<span data-ttu-id="a73e2-120">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a73e2-120">Specifies the name of a resource group.</span></span>
<span data-ttu-id="a73e2-121">如果您指定資源群組，此 Cmdlet 會在指定的資源群組下取得帳戶。</span><span class="sxs-lookup"><span data-stu-id="a73e2-121">If you specify a resource group, this cmdlet gets the accounts under the specified resource group.</span></span>

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

### <span data-ttu-id="a73e2-122">-Tag</span><span class="sxs-lookup"><span data-stu-id="a73e2-122">-Tag</span></span>
<span data-ttu-id="a73e2-123">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="a73e2-123">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a73e2-124">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"} 這個 Cmdlet 會取得包含此參數所指定之標記的帳戶。</span><span class="sxs-lookup"><span data-stu-id="a73e2-124">For example: @{key0="value0";key1=$null;key2="value2"} This cmdlet gets accounts that contain the tags that this parameter specifies.</span></span>

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

### <span data-ttu-id="a73e2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a73e2-125">CommonParameters</span></span>
<span data-ttu-id="a73e2-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a73e2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a73e2-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a73e2-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a73e2-128">輸入</span><span class="sxs-lookup"><span data-stu-id="a73e2-128">INPUTS</span></span>

### <span data-ttu-id="a73e2-129">System.object</span><span class="sxs-lookup"><span data-stu-id="a73e2-129">System.String</span></span>

### <span data-ttu-id="a73e2-130">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a73e2-130">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a73e2-131">輸出</span><span class="sxs-lookup"><span data-stu-id="a73e2-131">OUTPUTS</span></span>

### <span data-ttu-id="a73e2-132">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="a73e2-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="a73e2-133">筆記</span><span class="sxs-lookup"><span data-stu-id="a73e2-133">NOTES</span></span>

## <span data-ttu-id="a73e2-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="a73e2-134">RELATED LINKS</span></span>

[<span data-ttu-id="a73e2-135">新-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="a73e2-135">New-AzBatchAccount</span></span>](./New-AzBatchAccount.md)

[<span data-ttu-id="a73e2-136">移除-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="a73e2-136">Remove-AzBatchAccount</span></span>](./Remove-AzBatchAccount.md)

[<span data-ttu-id="a73e2-137">Set-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="a73e2-137">Set-AzBatchAccount</span></span>](./Set-AzBatchAccount.md)

[<span data-ttu-id="a73e2-138">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a73e2-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
