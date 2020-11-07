---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: E0E2617F-F6F1-434E-AD7C-27D309C2C3DA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 9b0e4b5da6ecd2877bab5860179cbaed80f43911
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625218"
---
# <span data-ttu-id="db643-101">Remove-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="db643-101">Remove-AzureRmDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="db643-102">摘要</span><span class="sxs-lookup"><span data-stu-id="db643-102">SYNOPSIS</span></span>
<span data-ttu-id="db643-103">從資料 Lake Analytics 帳戶移除資料來源。</span><span class="sxs-lookup"><span data-stu-id="db643-103">Removes a data source from a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db643-104">句法</span><span class="sxs-lookup"><span data-stu-id="db643-104">SYNTAX</span></span>

### <span data-ttu-id="db643-105">移除 Data Lake 儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="db643-105">Remove a Data Lake storage account</span></span>
```
Remove-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String> [-Force] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="db643-106">移除 Blob 儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="db643-106">Remove a Blob storage account</span></span>
```
Remove-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-Force] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="db643-107">說明</span><span class="sxs-lookup"><span data-stu-id="db643-107">DESCRIPTION</span></span>
<span data-ttu-id="db643-108">**AzureRmDataLakeAnalyticsDataSource** Cmdlet 會從 Azure Data Lake Analytics 帳戶中移除資料來源。</span><span class="sxs-lookup"><span data-stu-id="db643-108">The **Remove-AzureRmDataLakeAnalyticsDataSource** cmdlet removes a data source from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="db643-109">示例</span><span class="sxs-lookup"><span data-stu-id="db643-109">EXAMPLES</span></span>

### <span data-ttu-id="db643-110">範例1：移除資料來源</span><span class="sxs-lookup"><span data-stu-id="db643-110">Example 1: Remove a data source</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "AzureStorage01"
```

<span data-ttu-id="db643-111">這個命令會從名為 ContosoAdlAccount 的帳戶中移除名為 AzureStorage01 的資料來源。</span><span class="sxs-lookup"><span data-stu-id="db643-111">This command removes the data source named AzureStorage01 from the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="db643-112">參數</span><span class="sxs-lookup"><span data-stu-id="db643-112">PARAMETERS</span></span>

### <span data-ttu-id="db643-113">-帳戶</span><span class="sxs-lookup"><span data-stu-id="db643-113">-Account</span></span>
<span data-ttu-id="db643-114">指定 Data Lake Analytics 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="db643-114">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db643-115">-Blob</span><span class="sxs-lookup"><span data-stu-id="db643-115">-Blob</span></span>
<span data-ttu-id="db643-116">指定要移除之 AzureBlob 儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="db643-116">Specifies the name of the AzureBlob Storage account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove a Blob storage account
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db643-117">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="db643-117">-DataLakeStore</span></span>
<span data-ttu-id="db643-118">指定要移除的 AzureData Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="db643-118">Specifies the name of the AzureData Lake Store account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove a Data Lake storage account
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db643-119">-Force</span><span class="sxs-lookup"><span data-stu-id="db643-119">-Force</span></span>
<span data-ttu-id="db643-120">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="db643-120">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db643-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="db643-121">-PassThru</span></span>
<span data-ttu-id="db643-122">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="db643-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="db643-123">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="db643-123">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db643-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db643-124">-ResourceGroupName</span></span>
<span data-ttu-id="db643-125">指定資料 Lake Analytics 帳戶的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="db643-125">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db643-126">-確認</span><span class="sxs-lookup"><span data-stu-id="db643-126">-Confirm</span></span>
<span data-ttu-id="db643-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="db643-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db643-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db643-128">-WhatIf</span></span>
<span data-ttu-id="db643-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="db643-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db643-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="db643-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db643-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db643-131">-DefaultProfile</span></span>
<span data-ttu-id="db643-132">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="db643-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db643-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db643-133">CommonParameters</span></span>
<span data-ttu-id="db643-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="db643-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db643-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="db643-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db643-136">輸入</span><span class="sxs-lookup"><span data-stu-id="db643-136">INPUTS</span></span>

## <span data-ttu-id="db643-137">輸出</span><span class="sxs-lookup"><span data-stu-id="db643-137">OUTPUTS</span></span>

### <span data-ttu-id="db643-138">bool</span><span class="sxs-lookup"><span data-stu-id="db643-138">bool</span></span>
<span data-ttu-id="db643-139">如果已指定 PassThru，則會在作業完成時傳回 true。</span><span class="sxs-lookup"><span data-stu-id="db643-139">If PassThru is specified, returns true upon completion of the operation.</span></span>

## <span data-ttu-id="db643-140">筆記</span><span class="sxs-lookup"><span data-stu-id="db643-140">NOTES</span></span>

## <span data-ttu-id="db643-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="db643-141">RELATED LINKS</span></span>

[<span data-ttu-id="db643-142">附加 AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="db643-142">Add-AzureRmDataLakeAnalyticsDataSource</span></span>](./Add-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="db643-143">Set-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="db643-143">Set-AzureRmDataLakeAnalyticsDataSource</span></span>](./Set-AzureRmDataLakeAnalyticsDataSource.md)


