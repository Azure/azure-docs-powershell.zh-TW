---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControl.md
ms.openlocfilehash: 42472efdde4ccf96f12a0617d9a86175eed13d1c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98285356"
---
# <span data-ttu-id="f5e64-101">Get-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="f5e64-101">Get-AzAutomationSourceControl</span></span>

## <span data-ttu-id="f5e64-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f5e64-102">SYNOPSIS</span></span>
<span data-ttu-id="f5e64-103">取得 Azure 自動化來源控制項的清單。</span><span class="sxs-lookup"><span data-stu-id="f5e64-103">Gets a list of Azure Automation source controls.</span></span>

## <span data-ttu-id="f5e64-104">句法</span><span class="sxs-lookup"><span data-stu-id="f5e64-104">SYNTAX</span></span>

### <span data-ttu-id="f5e64-105">ByAll (預設) </span><span class="sxs-lookup"><span data-stu-id="f5e64-105">ByAll (Default)</span></span>
```
Get-AzAutomationSourceControl [-SourceType <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f5e64-106">ByName</span><span class="sxs-lookup"><span data-stu-id="f5e64-106">ByName</span></span>
```
Get-AzAutomationSourceControl -Name <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5e64-107">說明</span><span class="sxs-lookup"><span data-stu-id="f5e64-107">DESCRIPTION</span></span>
<span data-ttu-id="f5e64-108">Get-AzAutomationSourceControl Cmdlet 會取得自動化來源控制項。</span><span class="sxs-lookup"><span data-stu-id="f5e64-108">The Get-AzAutomationSourceControl cmdlet gets Automation source controls.</span></span>
<span data-ttu-id="f5e64-109">若要取得特定的來源控制項，請指定其名稱。</span><span class="sxs-lookup"><span data-stu-id="f5e64-109">To get a specific source control, specify its name.</span></span>

## <span data-ttu-id="f5e64-110">示例</span><span class="sxs-lookup"><span data-stu-id="f5e64-110">EXAMPLES</span></span>

### <span data-ttu-id="f5e64-111">範例1</span><span class="sxs-lookup"><span data-stu-id="f5e64-111">Example 1</span></span>
<span data-ttu-id="f5e64-112">這個命令會在名為 devAccount 的帳戶中取得名為 VSTSNative 的自動化來源控制。</span><span class="sxs-lookup"><span data-stu-id="f5e64-112">This command gets an Automation source control named VSTSNative in the account named devAccount.</span></span>


```powershell
PS C:\> Get-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name "VSTSNative" 


Name            SourceType Branch FolderPath  AutoSync PublishRunbook RepoUrl
----            ---------- ------ ----------  -------- -------------- -------
VSTSNative      VsoTfvc           /MyRunbooks False    True           https://contoso.visualstudio.com/_git/Fin...
```

## <span data-ttu-id="f5e64-113">參數</span><span class="sxs-lookup"><span data-stu-id="f5e64-113">PARAMETERS</span></span>

### <span data-ttu-id="f5e64-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f5e64-114">-AutomationAccountName</span></span>
<span data-ttu-id="f5e64-115">自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="f5e64-115">The automation account name.</span></span>

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

### <span data-ttu-id="f5e64-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5e64-116">-DefaultProfile</span></span>
<span data-ttu-id="f5e64-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f5e64-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5e64-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="f5e64-118">-Name</span></span>
<span data-ttu-id="f5e64-119">來源控制項名稱。</span><span class="sxs-lookup"><span data-stu-id="f5e64-119">The source control name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5e64-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5e64-120">-ResourceGroupName</span></span>
<span data-ttu-id="f5e64-121">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f5e64-121">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5e64-122">-SourceType</span><span class="sxs-lookup"><span data-stu-id="f5e64-122">-SourceType</span></span>
<span data-ttu-id="f5e64-123">來源控制項類型。</span><span class="sxs-lookup"><span data-stu-id="f5e64-123">The source control type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll
Aliases:
Accepted values: GitHub, VsoGit, VsoTfvc

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5e64-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5e64-124">CommonParameters</span></span>
<span data-ttu-id="f5e64-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f5e64-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5e64-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f5e64-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5e64-127">輸入</span><span class="sxs-lookup"><span data-stu-id="f5e64-127">INPUTS</span></span>

### <span data-ttu-id="f5e64-128">System.object</span><span class="sxs-lookup"><span data-stu-id="f5e64-128">System.String</span></span>

## <span data-ttu-id="f5e64-129">輸出</span><span class="sxs-lookup"><span data-stu-id="f5e64-129">OUTPUTS</span></span>

### <span data-ttu-id="f5e64-130">SourceControl 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f5e64-130">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="f5e64-131">筆記</span><span class="sxs-lookup"><span data-stu-id="f5e64-131">NOTES</span></span>

## <span data-ttu-id="f5e64-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="f5e64-132">RELATED LINKS</span></span>
