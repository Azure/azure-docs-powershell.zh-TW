---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: C583BECF-7FC2-4A1F-9788-5CB19E73956C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9464e811597ba0fe5bfe2d53643c7b788c9be71e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967516"
---
# <span data-ttu-id="56dff-101">Set-AzureAutomationRunbookDefinition</span><span class="sxs-lookup"><span data-stu-id="56dff-101">Set-AzureAutomationRunbookDefinition</span></span>

## <span data-ttu-id="56dff-102">摘要</span><span class="sxs-lookup"><span data-stu-id="56dff-102">SYNOPSIS</span></span>

<span data-ttu-id="56dff-103">更新 runbook 的草稿定義。</span><span class="sxs-lookup"><span data-stu-id="56dff-103">Updates the draft definition of a runbook.</span></span>

## <span data-ttu-id="56dff-104">句法</span><span class="sxs-lookup"><span data-stu-id="56dff-104">SYNTAX</span></span>

```
Set-AzureAutomationRunbookDefinition -Name <String> -Path <String> [-Overwrite] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="56dff-105">說明</span><span class="sxs-lookup"><span data-stu-id="56dff-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="56dff-106">**AzureAutomationRunbookDefinition** Cmdlet 會更新 Microsoft Azure 自動化 runbook 的草稿定義。</span><span class="sxs-lookup"><span data-stu-id="56dff-106">The **Set-AzureAutomationRunbookDefinition** cmdlet updates the draft definition of a Microsoft Azure Automation runbook.</span></span>
<span data-ttu-id="56dff-107">指定 Windows PowerShell 腳本 ( ps1) 檔案，該檔案包含成為草稿版 runbook 的 runbook。</span><span class="sxs-lookup"><span data-stu-id="56dff-107">Specify a Windows PowerShell script (.ps1) file that contains a runbook that becomes the draft runbook.</span></span>

<span data-ttu-id="56dff-108">如果草稿定義已存在，請使用 *Overwrite* 參數強制 Cmdlet 覆寫現有的草稿。</span><span class="sxs-lookup"><span data-stu-id="56dff-108">If a draft definition already exists, use the *Overwrite* parameter to force the cmdlet to overwrite the existing draft.</span></span>

## <span data-ttu-id="56dff-109">示例</span><span class="sxs-lookup"><span data-stu-id="56dff-109">EXAMPLES</span></span>

### <span data-ttu-id="56dff-110">範例1：覆寫現有的 runbook 草稿定義</span><span class="sxs-lookup"><span data-stu-id="56dff-110">Example 1: Overwrite an existing draft definition of a runbook</span></span>
```
PS C:\> Set-AzureAutomationRunbookDefinition -AutomationAccountName "Contoso17" -Name "Runbk01" -Path ".\App01.ps1" -Overwrite
```

<span data-ttu-id="56dff-111">這個命令會覆寫 runbook 的現有草稿定義。</span><span class="sxs-lookup"><span data-stu-id="56dff-111">This command overwrites the existing draft definition of a runbook.</span></span>

## <span data-ttu-id="56dff-112">參數</span><span class="sxs-lookup"><span data-stu-id="56dff-112">PARAMETERS</span></span>

### <span data-ttu-id="56dff-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="56dff-113">-AutomationAccountName</span></span>
<span data-ttu-id="56dff-114">指定自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="56dff-114">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="56dff-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="56dff-115">-Name</span></span>
<span data-ttu-id="56dff-116">指定名稱。</span><span class="sxs-lookup"><span data-stu-id="56dff-116">Specifies a name.</span></span>

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

### <span data-ttu-id="56dff-117">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="56dff-117">-Overwrite</span></span>
<span data-ttu-id="56dff-118">指出是否要覆寫現有的繪圖定義。</span><span class="sxs-lookup"><span data-stu-id="56dff-118">Indicates whether to overwrite an existing draft definition.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56dff-119">-Path</span><span class="sxs-lookup"><span data-stu-id="56dff-119">-Path</span></span>
<span data-ttu-id="56dff-120">指定 runbook 的路徑。</span><span class="sxs-lookup"><span data-stu-id="56dff-120">Specifies the path to a runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookPath

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56dff-121">-設定檔</span><span class="sxs-lookup"><span data-stu-id="56dff-121">-Profile</span></span>
<span data-ttu-id="56dff-122">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="56dff-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="56dff-123">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="56dff-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="56dff-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56dff-124">CommonParameters</span></span>
<span data-ttu-id="56dff-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="56dff-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56dff-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="56dff-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56dff-127">輸入</span><span class="sxs-lookup"><span data-stu-id="56dff-127">INPUTS</span></span>

## <span data-ttu-id="56dff-128">輸出</span><span class="sxs-lookup"><span data-stu-id="56dff-128">OUTPUTS</span></span>

### <span data-ttu-id="56dff-129">RunbookDefinition 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="56dff-129">Microsoft.Azure.Commands.Automation.Model.RunbookDefinition</span></span>

## <span data-ttu-id="56dff-130">筆記</span><span class="sxs-lookup"><span data-stu-id="56dff-130">NOTES</span></span>

## <span data-ttu-id="56dff-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="56dff-131">RELATED LINKS</span></span>

[<span data-ttu-id="56dff-132">AzureAutomationRunbookDefinition</span><span class="sxs-lookup"><span data-stu-id="56dff-132">Get-AzureAutomationRunbookDefinition</span></span>](./Get-AzureAutomationRunbookDefinition.md)


