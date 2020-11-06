---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: E0E2617F-F6F1-434E-AD7C-27D309C2C3DA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/remove-azurermdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 2707100452f9b64c093b4ae52c724e09f6cfe6e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448706"
---
# <span data-ttu-id="ed9c9-101">Remove-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="ed9c9-101">Remove-AzureRmDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="ed9c9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ed9c9-102">SYNOPSIS</span></span>
<span data-ttu-id="ed9c9-103">從資料 Lake Analytics 帳戶移除資料來源。</span><span class="sxs-lookup"><span data-stu-id="ed9c9-103">Removes a data source from a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed9c9-104">句法</span><span class="sxs-lookup"><span data-stu-id="ed9c9-104">SYNTAX</span></span>

### <span data-ttu-id="ed9c9-105">RemoveDataLakeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ed9c9-105">RemoveDataLakeStorageAccount</span></span>
```
Remove-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String> [-Force] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ed9c9-106">RemoveBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ed9c9-106">RemoveBlobStorageAccount</span></span>
```
Remove-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-Force] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ed9c9-107">說明</span><span class="sxs-lookup"><span data-stu-id="ed9c9-107">DESCRIPTION</span></span>
<span data-ttu-id="ed9c9-108">**AzureRmDataLakeAnalyticsDataSource** Cmdlet 會從 Azure Data Lake Analytics 帳戶中移除資料來源。</span><span class="sxs-lookup"><span data-stu-id="ed9c9-108">The **Remove-AzureRmDataLakeAnalyticsDataSource** cmdlet removes a data source from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="ed9c9-109">示例</span><span class="sxs-lookup"><span data-stu-id="ed9c9-109">EXAMPLES</span></span>

### <span data-ttu-id="ed9c9-110">範例1：移除資料來源</span><span class="sxs-lookup"><span data-stu-id="ed9c9-110">Example 1: Remove a data source</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "AzureStorage01"
```

<span data-ttu-id="ed9c9-111">這個命令會從名為 ContosoAdlAccount 的帳戶中移除名為 AzureStorage01 的資料來源。</span><span class="sxs-lookup"><span data-stu-id="ed9c9-111">This command removes the data source named AzureStorage01 from the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="ed9c9-112">參數</span><span class="sxs-lookup"><span data-stu-id="ed9c9-112">PARAMETERS</span></span>

### <span data-ttu-id="ed9c9-113">-帳戶</span><span class="sxs-lookup"><span data-stu-id="ed9c9-113">-Account</span></span>
<span data-ttu-id="ed9c9-114">指定 Data Lake Analytics 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="ed9c9-114">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed9c9-115">-Blob</span><span class="sxs-lookup"><span data-stu-id="ed9c9-115">-Blob</span></span>
<span data-ttu-id="ed9c9-116">指定要移除之 AzureBlob 儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="ed9c9-116">Specifies the name of the AzureBlob Storage account to remove.</span></span>

```yaml
Type: String
Parameter Sets: RemoveBlobStorageAccount
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed9c9-117">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ed9c9-117">-DataLakeStore</span></span>
<span data-ttu-id="ed9c9-118">指定要移除的 AzureData Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="ed9c9-118">Specifies the name of the AzureData Lake Store account to remove.</span></span>

```yaml
Type: String
Parameter Sets: RemoveDataLakeStorageAccount
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed9c9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed9c9-119">-DefaultProfile</span></span>
<span data-ttu-id="ed9c9-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="ed9c9-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ed9c9-121">-Force</span><span class="sxs-lookup"><span data-stu-id="ed9c9-121">-Force</span></span>
<span data-ttu-id="ed9c9-122">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="ed9c9-122">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed9c9-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ed9c9-123">-PassThru</span></span>
<span data-ttu-id="ed9c9-124">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="ed9c9-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ed9c9-125">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="ed9c9-125">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed9c9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed9c9-126">-ResourceGroupName</span></span>
<span data-ttu-id="ed9c9-127">指定資料 Lake Analytics 帳戶的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="ed9c9-127">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed9c9-128">-確認</span><span class="sxs-lookup"><span data-stu-id="ed9c9-128">-Confirm</span></span>
<span data-ttu-id="ed9c9-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ed9c9-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed9c9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed9c9-130">-WhatIf</span></span>
<span data-ttu-id="ed9c9-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ed9c9-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed9c9-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ed9c9-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed9c9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed9c9-133">CommonParameters</span></span>
<span data-ttu-id="ed9c9-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ed9c9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed9c9-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ed9c9-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed9c9-136">輸入</span><span class="sxs-lookup"><span data-stu-id="ed9c9-136">INPUTS</span></span>

### <span data-ttu-id="ed9c9-137">所有</span><span class="sxs-lookup"><span data-stu-id="ed9c9-137">None</span></span>
<span data-ttu-id="ed9c9-138">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="ed9c9-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ed9c9-139">輸出</span><span class="sxs-lookup"><span data-stu-id="ed9c9-139">OUTPUTS</span></span>

### <span data-ttu-id="ed9c9-140">bool</span><span class="sxs-lookup"><span data-stu-id="ed9c9-140">bool</span></span>
<span data-ttu-id="ed9c9-141">如果已指定 PassThru，則會在作業完成時傳回 true。</span><span class="sxs-lookup"><span data-stu-id="ed9c9-141">If PassThru is specified, returns true upon completion of the operation.</span></span>

## <span data-ttu-id="ed9c9-142">筆記</span><span class="sxs-lookup"><span data-stu-id="ed9c9-142">NOTES</span></span>

## <span data-ttu-id="ed9c9-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="ed9c9-143">RELATED LINKS</span></span>

[<span data-ttu-id="ed9c9-144">附加 AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="ed9c9-144">Add-AzureRmDataLakeAnalyticsDataSource</span></span>](./Add-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="ed9c9-145">Set-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="ed9c9-145">Set-AzureRmDataLakeAnalyticsDataSource</span></span>](./Set-AzureRmDataLakeAnalyticsDataSource.md)

