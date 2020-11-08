---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 5EB9E134-C789-47A5-9AF8-CD4A475559C2
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/stop-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Stop-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Stop-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 6825dc4a66e160590f420bf1c21b0dab0cd29d55
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956535"
---
# <span data-ttu-id="b7316-101">Stop-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="b7316-101">Stop-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="b7316-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b7316-102">SYNOPSIS</span></span>
<span data-ttu-id="b7316-103">取消作業。</span><span class="sxs-lookup"><span data-stu-id="b7316-103">Cancels a job.</span></span>

## <span data-ttu-id="b7316-104">句法</span><span class="sxs-lookup"><span data-stu-id="b7316-104">SYNTAX</span></span>

```
Stop-AzDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7316-105">說明</span><span class="sxs-lookup"><span data-stu-id="b7316-105">DESCRIPTION</span></span>
<span data-ttu-id="b7316-106">**AzDataLakeAnalyticsJob** Cmdlet 會取消 Azure Data Lake Analytics 作業。</span><span class="sxs-lookup"><span data-stu-id="b7316-106">The **Stop-AzDataLakeAnalyticsJob** cmdlet cancels an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="b7316-107">示例</span><span class="sxs-lookup"><span data-stu-id="b7316-107">EXAMPLES</span></span>

### <span data-ttu-id="b7316-108">範例1：取消作業</span><span class="sxs-lookup"><span data-stu-id="b7316-108">Example 1: Cancel a job</span></span>
```
PS C:\>Stop-AzDataLakeAnalyticsJob -Account "ContosoAdlAccout" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="b7316-109">這個命令會取消具有指定識別碼的作業。</span><span class="sxs-lookup"><span data-stu-id="b7316-109">This command cancels the job with the specified ID.</span></span>

## <span data-ttu-id="b7316-110">參數</span><span class="sxs-lookup"><span data-stu-id="b7316-110">PARAMETERS</span></span>

### <span data-ttu-id="b7316-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="b7316-111">-Account</span></span>
<span data-ttu-id="b7316-112">指定 Data Lake Analytics 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="b7316-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="b7316-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7316-113">-DefaultProfile</span></span>
<span data-ttu-id="b7316-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="b7316-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b7316-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b7316-115">-Force</span></span>
<span data-ttu-id="b7316-116">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="b7316-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b7316-117">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="b7316-117">-JobId</span></span>
<span data-ttu-id="b7316-118">指定要取消的作業識別碼。</span><span class="sxs-lookup"><span data-stu-id="b7316-118">Specifies the ID of the job to cancel.</span></span>

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

### <span data-ttu-id="b7316-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b7316-119">-PassThru</span></span>
<span data-ttu-id="b7316-120">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="b7316-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b7316-121">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="b7316-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b7316-122">-確認</span><span class="sxs-lookup"><span data-stu-id="b7316-122">-Confirm</span></span>
<span data-ttu-id="b7316-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b7316-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7316-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7316-124">-WhatIf</span></span>
<span data-ttu-id="b7316-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b7316-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7316-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b7316-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7316-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7316-127">CommonParameters</span></span>
<span data-ttu-id="b7316-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b7316-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7316-129">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b7316-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7316-130">輸入</span><span class="sxs-lookup"><span data-stu-id="b7316-130">INPUTS</span></span>

### <span data-ttu-id="b7316-131">System.object</span><span class="sxs-lookup"><span data-stu-id="b7316-131">System.String</span></span>

### <span data-ttu-id="b7316-132">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="b7316-132">System.Guid</span></span>

### <span data-ttu-id="b7316-133">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="b7316-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b7316-134">輸出</span><span class="sxs-lookup"><span data-stu-id="b7316-134">OUTPUTS</span></span>

### <span data-ttu-id="b7316-135">System.object</span><span class="sxs-lookup"><span data-stu-id="b7316-135">System.Boolean</span></span>

## <span data-ttu-id="b7316-136">筆記</span><span class="sxs-lookup"><span data-stu-id="b7316-136">NOTES</span></span>

## <span data-ttu-id="b7316-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="b7316-137">RELATED LINKS</span></span>

[<span data-ttu-id="b7316-138">AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="b7316-138">Get-AzDataLakeAnalyticsJob</span></span>](./Get-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="b7316-139">Submit-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="b7316-139">Submit-AzDataLakeAnalyticsJob</span></span>](./Submit-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="b7316-140">稍候-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="b7316-140">Wait-AzDataLakeAnalyticsJob</span></span>](./Wait-AzDataLakeAnalyticsJob.md)

