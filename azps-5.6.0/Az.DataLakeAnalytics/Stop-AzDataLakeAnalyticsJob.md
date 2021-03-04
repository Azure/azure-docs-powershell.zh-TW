---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 5EB9E134-C789-47A5-9AF8-CD4A475559C2
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/stop-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Stop-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Stop-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 3858c2ad6ca90716d5c9140949a683b9c409a105
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917761"
---
# <span data-ttu-id="d57a4-101">Stop-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d57a4-101">Stop-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="d57a4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d57a4-102">SYNOPSIS</span></span>
<span data-ttu-id="d57a4-103">取消工作。</span><span class="sxs-lookup"><span data-stu-id="d57a4-103">Cancels a job.</span></span>

## <span data-ttu-id="d57a4-104">語法</span><span class="sxs-lookup"><span data-stu-id="d57a4-104">SYNTAX</span></span>

```
Stop-AzDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d57a4-105">描述</span><span class="sxs-lookup"><span data-stu-id="d57a4-105">DESCRIPTION</span></span>
<span data-ttu-id="d57a4-106">**Stop-AzDataLakeAnalyticsJob** Cmdlet 會取消 Azure Data Lake Analytics 工作。</span><span class="sxs-lookup"><span data-stu-id="d57a4-106">The **Stop-AzDataLakeAnalyticsJob** cmdlet cancels an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="d57a4-107">例子</span><span class="sxs-lookup"><span data-stu-id="d57a4-107">EXAMPLES</span></span>

### <span data-ttu-id="d57a4-108">範例 1：取消工作</span><span class="sxs-lookup"><span data-stu-id="d57a4-108">Example 1: Cancel a job</span></span>
```
PS C:\>Stop-AzDataLakeAnalyticsJob -Account "ContosoAdlAccout" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="d57a4-109">此命令會取消具有指定識別碼的工作。</span><span class="sxs-lookup"><span data-stu-id="d57a4-109">This command cancels the job with the specified ID.</span></span>

## <span data-ttu-id="d57a4-110">參數</span><span class="sxs-lookup"><span data-stu-id="d57a4-110">PARAMETERS</span></span>

### <span data-ttu-id="d57a4-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="d57a4-111">-Account</span></span>
<span data-ttu-id="d57a4-112">指定 Data Lake Analytics 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="d57a4-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="d57a4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d57a4-113">-DefaultProfile</span></span>
<span data-ttu-id="d57a4-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="d57a4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d57a4-115">-強制</span><span class="sxs-lookup"><span data-stu-id="d57a4-115">-Force</span></span>
<span data-ttu-id="d57a4-116">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="d57a4-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d57a4-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="d57a4-117">-JobId</span></span>
<span data-ttu-id="d57a4-118">指定要取消的工作識別碼。</span><span class="sxs-lookup"><span data-stu-id="d57a4-118">Specifies the ID of the job to cancel.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d57a4-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d57a4-119">-PassThru</span></span>
<span data-ttu-id="d57a4-120">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="d57a4-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d57a4-121">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="d57a4-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d57a4-122">-確認</span><span class="sxs-lookup"><span data-stu-id="d57a4-122">-Confirm</span></span>
<span data-ttu-id="d57a4-123">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d57a4-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d57a4-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d57a4-124">-WhatIf</span></span>
<span data-ttu-id="d57a4-125">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d57a4-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d57a4-126">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d57a4-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d57a4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d57a4-127">CommonParameters</span></span>
<span data-ttu-id="d57a4-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d57a4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d57a4-129">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="d57a4-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d57a4-130">輸入</span><span class="sxs-lookup"><span data-stu-id="d57a4-130">INPUTS</span></span>

### <span data-ttu-id="d57a4-131">System.String</span><span class="sxs-lookup"><span data-stu-id="d57a4-131">System.String</span></span>

### <span data-ttu-id="d57a4-132">System.Guid</span><span class="sxs-lookup"><span data-stu-id="d57a4-132">System.Guid</span></span>

### <span data-ttu-id="d57a4-133">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d57a4-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d57a4-134">輸出</span><span class="sxs-lookup"><span data-stu-id="d57a4-134">OUTPUTS</span></span>

### <span data-ttu-id="d57a4-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d57a4-135">System.Boolean</span></span>

## <span data-ttu-id="d57a4-136">筆記</span><span class="sxs-lookup"><span data-stu-id="d57a4-136">NOTES</span></span>

## <span data-ttu-id="d57a4-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="d57a4-137">RELATED LINKS</span></span>

[<span data-ttu-id="d57a4-138">Get-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d57a4-138">Get-AzDataLakeAnalyticsJob</span></span>](./Get-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="d57a4-139">Submit-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d57a4-139">Submit-AzDataLakeAnalyticsJob</span></span>](./Submit-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="d57a4-140">Wait-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d57a4-140">Wait-AzDataLakeAnalyticsJob</span></span>](./Wait-AzDataLakeAnalyticsJob.md)


