---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 66740917-E8BB-44ED-9CBB-9825BD1840E4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5b049d770dbcee8b7cea56dbadbf7d4071c344cc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967808"
---
# <span data-ttu-id="406f0-101">Get-AzureAutomationRunbookDefinition</span><span class="sxs-lookup"><span data-stu-id="406f0-101">Get-AzureAutomationRunbookDefinition</span></span>

## <span data-ttu-id="406f0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="406f0-102">SYNOPSIS</span></span>

<span data-ttu-id="406f0-103">取得 runbook 定義。</span><span class="sxs-lookup"><span data-stu-id="406f0-103">Gets a runbook definition.</span></span>

## <span data-ttu-id="406f0-104">句法</span><span class="sxs-lookup"><span data-stu-id="406f0-104">SYNTAX</span></span>

```
Get-AzureAutomationRunbookDefinition -Name <String> [-Slot <String>] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="406f0-105">說明</span><span class="sxs-lookup"><span data-stu-id="406f0-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="406f0-106">**AzureAutomationRunbookDefinition** Cmdlet 會取得草案定義、已發佈的定義，或 Azure 自動化 runbook 的兩個定義。</span><span class="sxs-lookup"><span data-stu-id="406f0-106">The **Get-AzureAutomationRunbookDefinition** cmdlet gets the draft definition, the published definition, or both definitions of an Azure Automation runbook.</span></span>
<span data-ttu-id="406f0-107">根據預設，會傳回發佈的版本。</span><span class="sxs-lookup"><span data-stu-id="406f0-107">By default, the published version is returned.</span></span>

## <span data-ttu-id="406f0-108">示例</span><span class="sxs-lookup"><span data-stu-id="406f0-108">EXAMPLES</span></span>

### <span data-ttu-id="406f0-109">範例1：取得 runbook 定義</span><span class="sxs-lookup"><span data-stu-id="406f0-109">Example 1: Get a runbook definition</span></span>
```
PS C:\> Get-AzureAutomationRunbookDefinition -AutomationAccountName "Contoso17" -Name "RunbookDef01" -Slot "Published"
```

<span data-ttu-id="406f0-110">這個命令會取得 Azure 自動化帳戶（名為 Contoso17）中名為 RunbookDef01 的 runbook 的發佈 runbook 定義。</span><span class="sxs-lookup"><span data-stu-id="406f0-110">This command gets the published runbook definition of the runbook named RunbookDef01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="406f0-111">參數</span><span class="sxs-lookup"><span data-stu-id="406f0-111">PARAMETERS</span></span>

### <span data-ttu-id="406f0-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="406f0-112">-AutomationAccountName</span></span>
<span data-ttu-id="406f0-113">指定自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="406f0-113">Specifies the name of an Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="406f0-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="406f0-114">-Name</span></span>
<span data-ttu-id="406f0-115">指定 runbook 的名稱。</span><span class="sxs-lookup"><span data-stu-id="406f0-115">Specifies the name of a runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="406f0-116">-設定檔</span><span class="sxs-lookup"><span data-stu-id="406f0-116">-Profile</span></span>
<span data-ttu-id="406f0-117">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="406f0-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="406f0-118">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="406f0-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="406f0-119">-槽</span><span class="sxs-lookup"><span data-stu-id="406f0-119">-Slot</span></span>
<span data-ttu-id="406f0-120">指定槽。</span><span class="sxs-lookup"><span data-stu-id="406f0-120">Specifies the slot.</span></span>
<span data-ttu-id="406f0-121">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="406f0-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="406f0-122">草案</span><span class="sxs-lookup"><span data-stu-id="406f0-122">Draft</span></span>
- <span data-ttu-id="406f0-123">時間</span><span class="sxs-lookup"><span data-stu-id="406f0-123">Published</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="406f0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="406f0-124">CommonParameters</span></span>
<span data-ttu-id="406f0-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="406f0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="406f0-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="406f0-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="406f0-127">輸入</span><span class="sxs-lookup"><span data-stu-id="406f0-127">INPUTS</span></span>

## <span data-ttu-id="406f0-128">輸出</span><span class="sxs-lookup"><span data-stu-id="406f0-128">OUTPUTS</span></span>

## <span data-ttu-id="406f0-129">筆記</span><span class="sxs-lookup"><span data-stu-id="406f0-129">NOTES</span></span>

## <span data-ttu-id="406f0-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="406f0-130">RELATED LINKS</span></span>

[<span data-ttu-id="406f0-131">Set-AzureAutomationRunbookDefinition</span><span class="sxs-lookup"><span data-stu-id="406f0-131">Set-AzureAutomationRunbookDefinition</span></span>](./Set-AzureAutomationRunbookDefinition.md)


