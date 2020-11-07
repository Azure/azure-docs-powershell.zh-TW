---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 82C7B128-8818-4390-B1A5-CB40AC9D53CA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchAccount.md
ms.openlocfilehash: ed44fa5960935bbe353d775a426e023512327e7f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624217"
---
# <span data-ttu-id="40513-101">New-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="40513-101">New-AzureRmBatchAccount</span></span>

## <span data-ttu-id="40513-102">摘要</span><span class="sxs-lookup"><span data-stu-id="40513-102">SYNOPSIS</span></span>
<span data-ttu-id="40513-103">建立 Batch 帳戶。</span><span class="sxs-lookup"><span data-stu-id="40513-103">Creates a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40513-104">句法</span><span class="sxs-lookup"><span data-stu-id="40513-104">SYNTAX</span></span>

```
New-AzureRmBatchAccount [-AccountName] <String> [-Location] <String> [-ResourceGroupName] <String>
 [[-AutoStorageAccountId] <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="40513-105">說明</span><span class="sxs-lookup"><span data-stu-id="40513-105">DESCRIPTION</span></span>
<span data-ttu-id="40513-106">**新的-AzureRmBatchAccount** Cmdlet 會針對指定的資源群組和位置建立 Azure Batch 帳戶。</span><span class="sxs-lookup"><span data-stu-id="40513-106">The **New-AzureRmBatchAccount** cmdlet creates an Azure Batch account for the specified resource group and location.</span></span>

## <span data-ttu-id="40513-107">示例</span><span class="sxs-lookup"><span data-stu-id="40513-107">EXAMPLES</span></span>

### <span data-ttu-id="40513-108">範例1：建立批次帳戶</span><span class="sxs-lookup"><span data-stu-id="40513-108">Example 1: Create a Batch account</span></span>
```
PS C:\>New-AzureRmBatchAccount -AccountName "pfuller" -ResourceGroupName "ResourceGroup03" -Location "WestUS"
AccountName                  : pfuller
Location                     : westus
ResourceGroupName            : ResourceGroup03
CoreQuota                    : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="40513-109">這個命令會使用 [西部美國] 位置中的 [ResourceGroup03] 資源群組，建立名為 pfuller 的批次帳戶。</span><span class="sxs-lookup"><span data-stu-id="40513-109">This command creates a Batch account named pfuller using the ResourceGroup03 resource group in the West US location.</span></span>

## <span data-ttu-id="40513-110">參數</span><span class="sxs-lookup"><span data-stu-id="40513-110">PARAMETERS</span></span>

### <span data-ttu-id="40513-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="40513-111">-AccountName</span></span>
<span data-ttu-id="40513-112">指定此 Cmdlet 所建立之 Batch 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="40513-112">Specifies the name of the Batch account that this cmdlet creates.</span></span>

<span data-ttu-id="40513-113">Batch 帳戶名稱長度必須介於3到24個字元之間，且只包含數位和小寫字母。</span><span class="sxs-lookup"><span data-stu-id="40513-113">Batch account names must be between 3 and 24 characters long and contain only numbers and lowercase letters.</span></span>

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

### <span data-ttu-id="40513-114">-AutoStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="40513-114">-AutoStorageAccountId</span></span>
<span data-ttu-id="40513-115">指定要用於自動儲存的儲存空間帳戶的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="40513-115">Specifies the resource ID of the storage account to be used for auto storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40513-116">-位置</span><span class="sxs-lookup"><span data-stu-id="40513-116">-Location</span></span>
<span data-ttu-id="40513-117">指定此 Cmdlet 建立帳戶的地區。</span><span class="sxs-lookup"><span data-stu-id="40513-117">Specifies the region where this cmdlet creates the account.</span></span>
<span data-ttu-id="40513-118">如需詳細資訊，請參閱 [Azure 地區](https://azure.microsoft.com/en-us/regions)。</span><span class="sxs-lookup"><span data-stu-id="40513-118">For more information, see [Azure Regions](https://azure.microsoft.com/en-us/regions).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40513-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40513-119">-ResourceGroupName</span></span>
<span data-ttu-id="40513-120">指定此 Cmdlet 在其中建立帳戶的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="40513-120">Specifies the name of the resource group in which this cmdlet creates the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40513-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="40513-121">-Tag</span></span>
<span data-ttu-id="40513-122">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="40513-122">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="40513-123">例如：</span><span class="sxs-lookup"><span data-stu-id="40513-123">For example:</span></span>

<span data-ttu-id="40513-124">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="40513-124">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40513-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40513-125">-DefaultProfile</span></span>
<span data-ttu-id="40513-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="40513-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40513-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40513-127">CommonParameters</span></span>
<span data-ttu-id="40513-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="40513-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40513-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="40513-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40513-130">輸入</span><span class="sxs-lookup"><span data-stu-id="40513-130">INPUTS</span></span>

## <span data-ttu-id="40513-131">輸出</span><span class="sxs-lookup"><span data-stu-id="40513-131">OUTPUTS</span></span>

### <span data-ttu-id="40513-132">BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="40513-132">BatchAccountContext</span></span>

## <span data-ttu-id="40513-133">筆記</span><span class="sxs-lookup"><span data-stu-id="40513-133">NOTES</span></span>

## <span data-ttu-id="40513-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="40513-134">RELATED LINKS</span></span>

[<span data-ttu-id="40513-135">AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="40513-135">Get-AzureRmBatchAccount</span></span>](./Get-AzureRmBatchAccount.md)

[<span data-ttu-id="40513-136">移除-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="40513-136">Remove-AzureRmBatchAccount</span></span>](./Remove-AzureRmBatchAccount.md)

[<span data-ttu-id="40513-137">Set-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="40513-137">Set-AzureRmBatchAccount</span></span>](./Set-AzureRmBatchAccount.md)

[<span data-ttu-id="40513-138">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="40513-138">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)
