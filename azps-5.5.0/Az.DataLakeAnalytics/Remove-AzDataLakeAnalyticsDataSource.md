---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: E0E2617F-F6F1-434E-AD7C-27D309C2C3DA
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsDataSource.md
ms.openlocfilehash: dfdd338fd5b49813d17e089755b419605761af3a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100129478"
---
# <span data-ttu-id="78242-101">Remove-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="78242-101">Remove-AzDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="78242-102">摘要</span><span class="sxs-lookup"><span data-stu-id="78242-102">SYNOPSIS</span></span>
<span data-ttu-id="78242-103">從資料 Lake Analytics 帳戶移除資料來源。</span><span class="sxs-lookup"><span data-stu-id="78242-103">Removes a data source from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="78242-104">句法</span><span class="sxs-lookup"><span data-stu-id="78242-104">SYNTAX</span></span>

### <span data-ttu-id="78242-105">RemoveDataLakeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="78242-105">RemoveDataLakeStorageAccount</span></span>
```
Remove-AzDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String> [-Force] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="78242-106">RemoveBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="78242-106">RemoveBlobStorageAccount</span></span>
```
Remove-AzDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-Force] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="78242-107">說明</span><span class="sxs-lookup"><span data-stu-id="78242-107">DESCRIPTION</span></span>
<span data-ttu-id="78242-108">**AzDataLakeAnalyticsDataSource** Cmdlet 會從 Azure Data Lake Analytics 帳戶中移除資料來源。</span><span class="sxs-lookup"><span data-stu-id="78242-108">The **Remove-AzDataLakeAnalyticsDataSource** cmdlet removes a data source from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="78242-109">示例</span><span class="sxs-lookup"><span data-stu-id="78242-109">EXAMPLES</span></span>

### <span data-ttu-id="78242-110">範例1：移除資料來源</span><span class="sxs-lookup"><span data-stu-id="78242-110">Example 1: Remove a data source</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "AzureStorage01"
```

<span data-ttu-id="78242-111">這個命令會從名為 ContosoAdlAccount 的帳戶中移除名為 AzureStorage01 的資料來源。</span><span class="sxs-lookup"><span data-stu-id="78242-111">This command removes the data source named AzureStorage01 from the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="78242-112">參數</span><span class="sxs-lookup"><span data-stu-id="78242-112">PARAMETERS</span></span>

### <span data-ttu-id="78242-113">-帳戶</span><span class="sxs-lookup"><span data-stu-id="78242-113">-Account</span></span>
<span data-ttu-id="78242-114">指定 Data Lake Analytics 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="78242-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="78242-115">-Blob</span><span class="sxs-lookup"><span data-stu-id="78242-115">-Blob</span></span>
<span data-ttu-id="78242-116">指定要移除之 AzureBlob 儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="78242-116">Specifies the name of the AzureBlob Storage account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBlobStorageAccount
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78242-117">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="78242-117">-DataLakeStore</span></span>
<span data-ttu-id="78242-118">指定要移除的 AzureData Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="78242-118">Specifies the name of the AzureData Lake Store account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveDataLakeStorageAccount
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78242-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78242-119">-DefaultProfile</span></span>
<span data-ttu-id="78242-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="78242-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="78242-121">-Force</span><span class="sxs-lookup"><span data-stu-id="78242-121">-Force</span></span>
<span data-ttu-id="78242-122">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="78242-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="78242-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="78242-123">-PassThru</span></span>
<span data-ttu-id="78242-124">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="78242-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="78242-125">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="78242-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="78242-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78242-126">-ResourceGroupName</span></span>
<span data-ttu-id="78242-127">指定資料 Lake Analytics 帳戶的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="78242-127">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="78242-128">-確認</span><span class="sxs-lookup"><span data-stu-id="78242-128">-Confirm</span></span>
<span data-ttu-id="78242-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="78242-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78242-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78242-130">-WhatIf</span></span>
<span data-ttu-id="78242-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="78242-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78242-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="78242-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78242-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78242-133">CommonParameters</span></span>
<span data-ttu-id="78242-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="78242-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78242-135">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="78242-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78242-136">輸入</span><span class="sxs-lookup"><span data-stu-id="78242-136">INPUTS</span></span>

### <span data-ttu-id="78242-137">System.object</span><span class="sxs-lookup"><span data-stu-id="78242-137">System.String</span></span>

## <span data-ttu-id="78242-138">輸出</span><span class="sxs-lookup"><span data-stu-id="78242-138">OUTPUTS</span></span>

### <span data-ttu-id="78242-139">System.object</span><span class="sxs-lookup"><span data-stu-id="78242-139">System.Boolean</span></span>

## <span data-ttu-id="78242-140">筆記</span><span class="sxs-lookup"><span data-stu-id="78242-140">NOTES</span></span>

## <span data-ttu-id="78242-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="78242-141">RELATED LINKS</span></span>

[<span data-ttu-id="78242-142">附加 AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="78242-142">Add-AzDataLakeAnalyticsDataSource</span></span>](./Add-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="78242-143">Set-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="78242-143">Set-AzDataLakeAnalyticsDataSource</span></span>](./Set-AzDataLakeAnalyticsDataSource.md)


