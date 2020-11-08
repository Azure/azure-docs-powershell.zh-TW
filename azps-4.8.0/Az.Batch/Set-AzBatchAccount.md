---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 9BEE5888-304D-4438-BE97-D1FE254AEE98
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchAccount.md
ms.openlocfilehash: 44627bd5ffa7340a10866605598d981b10f35a58
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970624"
---
# <span data-ttu-id="7bf59-101">Set-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="7bf59-101">Set-AzBatchAccount</span></span>

## <span data-ttu-id="7bf59-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7bf59-102">SYNOPSIS</span></span>
<span data-ttu-id="7bf59-103">更新批次帳戶。</span><span class="sxs-lookup"><span data-stu-id="7bf59-103">Updates a Batch account.</span></span>

## <span data-ttu-id="7bf59-104">句法</span><span class="sxs-lookup"><span data-stu-id="7bf59-104">SYNTAX</span></span>

```
Set-AzBatchAccount [-AccountName] <String> [-Tag] <Hashtable> [-ResourceGroupName <String>]
 [-AutoStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7bf59-105">說明</span><span class="sxs-lookup"><span data-stu-id="7bf59-105">DESCRIPTION</span></span>
<span data-ttu-id="7bf59-106">**AzBatchAccount** Cmdlet 會更新 Azure Batch 帳戶。</span><span class="sxs-lookup"><span data-stu-id="7bf59-106">The **Set-AzBatchAccount** cmdlet updates an Azure Batch account.</span></span>
<span data-ttu-id="7bf59-107">這個 Cmdlet 目前只能更新標記。</span><span class="sxs-lookup"><span data-stu-id="7bf59-107">Currently, this cmdlet can update only tags.</span></span>

## <span data-ttu-id="7bf59-108">示例</span><span class="sxs-lookup"><span data-stu-id="7bf59-108">EXAMPLES</span></span>

### <span data-ttu-id="7bf59-109">範例1：更新批次帳戶上的標籤</span><span class="sxs-lookup"><span data-stu-id="7bf59-109">Example 1: Update the tags on a Batch account</span></span>
```
PS C:\>Set-AzBatchAccount -AccountName "cmdletexample" -Tag @{key0="value0";key1=$null;key2="value2"}
AccountName                  : cmdletexample
Location                     : westus
ResourceGroupName            : CmdletExampleRG
DedicatedCoreQuota           : 20
LowPriorityCoreQuota         : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
                               Name  Value
                               ====  ======
                               key0  value0
                               key1
                               key2  value2
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="7bf59-110">這個命令會更新名為 pfuller 的帳戶上的標記。</span><span class="sxs-lookup"><span data-stu-id="7bf59-110">This command updates the tags on the account named pfuller.</span></span>

## <span data-ttu-id="7bf59-111">參數</span><span class="sxs-lookup"><span data-stu-id="7bf59-111">PARAMETERS</span></span>

### <span data-ttu-id="7bf59-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7bf59-112">-AccountName</span></span>
<span data-ttu-id="7bf59-113">指定此 Cmdlet 更新之批次帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="7bf59-113">Specifies the name of the Batch account that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bf59-114">-AutoStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="7bf59-114">-AutoStorageAccountId</span></span>
<span data-ttu-id="7bf59-115">指定要用於自動儲存的儲存空間帳戶的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="7bf59-115">Specifies the resource ID of the storage account to be used for auto storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bf59-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bf59-116">-DefaultProfile</span></span>
<span data-ttu-id="7bf59-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7bf59-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7bf59-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bf59-118">-ResourceGroupName</span></span>
<span data-ttu-id="7bf59-119">指定此 Cmdlet 更新之帳戶的資源群組。</span><span class="sxs-lookup"><span data-stu-id="7bf59-119">Specifies the resource group of the account that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bf59-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="7bf59-120">-Tag</span></span>
<span data-ttu-id="7bf59-121">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="7bf59-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7bf59-122">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="7bf59-122">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bf59-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bf59-123">CommonParameters</span></span>
<span data-ttu-id="7bf59-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7bf59-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bf59-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7bf59-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bf59-126">輸入</span><span class="sxs-lookup"><span data-stu-id="7bf59-126">INPUTS</span></span>

### <span data-ttu-id="7bf59-127">System.object</span><span class="sxs-lookup"><span data-stu-id="7bf59-127">System.String</span></span>

### <span data-ttu-id="7bf59-128">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7bf59-128">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7bf59-129">輸出</span><span class="sxs-lookup"><span data-stu-id="7bf59-129">OUTPUTS</span></span>

### <span data-ttu-id="7bf59-130">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="7bf59-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="7bf59-131">筆記</span><span class="sxs-lookup"><span data-stu-id="7bf59-131">NOTES</span></span>

## <span data-ttu-id="7bf59-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="7bf59-132">RELATED LINKS</span></span>

[<span data-ttu-id="7bf59-133">AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="7bf59-133">Get-AzBatchAccount</span></span>](./Get-AzBatchAccount.md)

[<span data-ttu-id="7bf59-134">新-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="7bf59-134">New-AzBatchAccount</span></span>](./New-AzBatchAccount.md)

[<span data-ttu-id="7bf59-135">移除-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="7bf59-135">Remove-AzBatchAccount</span></span>](./Remove-AzBatchAccount.md)

[<span data-ttu-id="7bf59-136">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7bf59-136">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)