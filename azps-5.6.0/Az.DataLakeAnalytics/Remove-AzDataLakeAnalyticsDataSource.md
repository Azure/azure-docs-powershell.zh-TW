---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: E0E2617F-F6F1-434E-AD7C-27D309C2C3DA
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsDataSource.md
ms.openlocfilehash: d5ea5e1131768c747a959af97ed541daefd4587b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908565"
---
# <span data-ttu-id="93265-101">Remove-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="93265-101">Remove-AzDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="93265-102">簡介</span><span class="sxs-lookup"><span data-stu-id="93265-102">SYNOPSIS</span></span>
<span data-ttu-id="93265-103">從 Data Lake Analytics 帳戶移除資料來源。</span><span class="sxs-lookup"><span data-stu-id="93265-103">Removes a data source from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="93265-104">語法</span><span class="sxs-lookup"><span data-stu-id="93265-104">SYNTAX</span></span>

### <span data-ttu-id="93265-105">RemoveDataLakeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="93265-105">RemoveDataLakeStorageAccount</span></span>
```
Remove-AzDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String> [-Force] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="93265-106">RemoveBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="93265-106">RemoveBlobStorageAccount</span></span>
```
Remove-AzDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-Force] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="93265-107">描述</span><span class="sxs-lookup"><span data-stu-id="93265-107">DESCRIPTION</span></span>
<span data-ttu-id="93265-108">**Remove-AzDataLakeAnalyticsDataSource** Cmdlet 會從 Azure Data Lake Analytics 帳戶移除資料來源。</span><span class="sxs-lookup"><span data-stu-id="93265-108">The **Remove-AzDataLakeAnalyticsDataSource** cmdlet removes a data source from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="93265-109">例子</span><span class="sxs-lookup"><span data-stu-id="93265-109">EXAMPLES</span></span>

### <span data-ttu-id="93265-110">範例 1：移除資料來源</span><span class="sxs-lookup"><span data-stu-id="93265-110">Example 1: Remove a data source</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "AzureStorage01"
```

<span data-ttu-id="93265-111">此命令會從名為 ContosoAdlAccount的帳戶移除名為 AzureStorage01 的資料來源。</span><span class="sxs-lookup"><span data-stu-id="93265-111">This command removes the data source named AzureStorage01 from the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="93265-112">參數</span><span class="sxs-lookup"><span data-stu-id="93265-112">PARAMETERS</span></span>

### <span data-ttu-id="93265-113">-帳戶</span><span class="sxs-lookup"><span data-stu-id="93265-113">-Account</span></span>
<span data-ttu-id="93265-114">指定 Data Lake Analytics 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="93265-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="93265-115">-Blob</span><span class="sxs-lookup"><span data-stu-id="93265-115">-Blob</span></span>
<span data-ttu-id="93265-116">指定要移除的 AzureBlob 儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="93265-116">Specifies the name of the AzureBlob Storage account to remove.</span></span>

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

### <span data-ttu-id="93265-117">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="93265-117">-DataLakeStore</span></span>
<span data-ttu-id="93265-118">指定要移除的 AzureData Lake Store 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="93265-118">Specifies the name of the AzureData Lake Store account to remove.</span></span>

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

### <span data-ttu-id="93265-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93265-119">-DefaultProfile</span></span>
<span data-ttu-id="93265-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="93265-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="93265-121">-強制</span><span class="sxs-lookup"><span data-stu-id="93265-121">-Force</span></span>
<span data-ttu-id="93265-122">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="93265-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="93265-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="93265-123">-PassThru</span></span>
<span data-ttu-id="93265-124">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="93265-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="93265-125">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="93265-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="93265-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93265-126">-ResourceGroupName</span></span>
<span data-ttu-id="93265-127">指定 Data Lake Analytics 帳戶的資源組名。</span><span class="sxs-lookup"><span data-stu-id="93265-127">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="93265-128">-確認</span><span class="sxs-lookup"><span data-stu-id="93265-128">-Confirm</span></span>
<span data-ttu-id="93265-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="93265-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93265-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93265-130">-WhatIf</span></span>
<span data-ttu-id="93265-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="93265-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93265-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="93265-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93265-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93265-133">CommonParameters</span></span>
<span data-ttu-id="93265-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="93265-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93265-135">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="93265-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93265-136">輸入</span><span class="sxs-lookup"><span data-stu-id="93265-136">INPUTS</span></span>

### <span data-ttu-id="93265-137">System.String</span><span class="sxs-lookup"><span data-stu-id="93265-137">System.String</span></span>

## <span data-ttu-id="93265-138">輸出</span><span class="sxs-lookup"><span data-stu-id="93265-138">OUTPUTS</span></span>

### <span data-ttu-id="93265-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="93265-139">System.Boolean</span></span>

## <span data-ttu-id="93265-140">筆記</span><span class="sxs-lookup"><span data-stu-id="93265-140">NOTES</span></span>

## <span data-ttu-id="93265-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="93265-141">RELATED LINKS</span></span>

[<span data-ttu-id="93265-142">Add-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="93265-142">Add-AzDataLakeAnalyticsDataSource</span></span>](./Add-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="93265-143">Set-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="93265-143">Set-AzDataLakeAnalyticsDataSource</span></span>](./Set-AzDataLakeAnalyticsDataSource.md)


