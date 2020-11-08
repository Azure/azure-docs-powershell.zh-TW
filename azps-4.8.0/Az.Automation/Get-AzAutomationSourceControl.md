---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControl.md
ms.openlocfilehash: 42472efdde4ccf96f12a0617d9a86175eed13d1c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128586"
---
# <span data-ttu-id="daefc-101">Get-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="daefc-101">Get-AzAutomationSourceControl</span></span>

## <span data-ttu-id="daefc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="daefc-102">SYNOPSIS</span></span>
<span data-ttu-id="daefc-103">取得 Azure 自動化來源控制項的清單。</span><span class="sxs-lookup"><span data-stu-id="daefc-103">Gets a list of Azure Automation source controls.</span></span>

## <span data-ttu-id="daefc-104">句法</span><span class="sxs-lookup"><span data-stu-id="daefc-104">SYNTAX</span></span>

### <span data-ttu-id="daefc-105">ByAll (預設) </span><span class="sxs-lookup"><span data-stu-id="daefc-105">ByAll (Default)</span></span>
```
Get-AzAutomationSourceControl [-SourceType <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="daefc-106">ByName</span><span class="sxs-lookup"><span data-stu-id="daefc-106">ByName</span></span>
```
Get-AzAutomationSourceControl -Name <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="daefc-107">說明</span><span class="sxs-lookup"><span data-stu-id="daefc-107">DESCRIPTION</span></span>
<span data-ttu-id="daefc-108">Get-AzAutomationSourceControl Cmdlet 會取得自動化來源控制項。</span><span class="sxs-lookup"><span data-stu-id="daefc-108">The Get-AzAutomationSourceControl cmdlet gets Automation source controls.</span></span>
<span data-ttu-id="daefc-109">若要取得特定的來源控制項，請指定其名稱。</span><span class="sxs-lookup"><span data-stu-id="daefc-109">To get a specific source control, specify its name.</span></span>

## <span data-ttu-id="daefc-110">示例</span><span class="sxs-lookup"><span data-stu-id="daefc-110">EXAMPLES</span></span>

### <span data-ttu-id="daefc-111">範例1</span><span class="sxs-lookup"><span data-stu-id="daefc-111">Example 1</span></span>
<span data-ttu-id="daefc-112">這個命令會在名為 devAccount 的帳戶中取得名為 VSTSNative 的自動化來源控制。</span><span class="sxs-lookup"><span data-stu-id="daefc-112">This command gets an Automation source control named VSTSNative in the account named devAccount.</span></span>


```powershell
PS C:\> Get-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name "VSTSNative" 


Name            SourceType Branch FolderPath  AutoSync PublishRunbook RepoUrl
----            ---------- ------ ----------  -------- -------------- -------
VSTSNative      VsoTfvc           /MyRunbooks False    True           https://contoso.visualstudio.com/_git/Fin...
```

## <span data-ttu-id="daefc-113">參數</span><span class="sxs-lookup"><span data-stu-id="daefc-113">PARAMETERS</span></span>

### <span data-ttu-id="daefc-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="daefc-114">-AutomationAccountName</span></span>
<span data-ttu-id="daefc-115">自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="daefc-115">The automation account name.</span></span>

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

### <span data-ttu-id="daefc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="daefc-116">-DefaultProfile</span></span>
<span data-ttu-id="daefc-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="daefc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="daefc-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="daefc-118">-Name</span></span>
<span data-ttu-id="daefc-119">來源控制項名稱。</span><span class="sxs-lookup"><span data-stu-id="daefc-119">The source control name.</span></span>

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

### <span data-ttu-id="daefc-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="daefc-120">-ResourceGroupName</span></span>
<span data-ttu-id="daefc-121">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="daefc-121">The resource group name.</span></span>

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

### <span data-ttu-id="daefc-122">-SourceType</span><span class="sxs-lookup"><span data-stu-id="daefc-122">-SourceType</span></span>
<span data-ttu-id="daefc-123">來源控制項類型。</span><span class="sxs-lookup"><span data-stu-id="daefc-123">The source control type.</span></span>

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

### <span data-ttu-id="daefc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daefc-124">CommonParameters</span></span>
<span data-ttu-id="daefc-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="daefc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daefc-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="daefc-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daefc-127">輸入</span><span class="sxs-lookup"><span data-stu-id="daefc-127">INPUTS</span></span>

### <span data-ttu-id="daefc-128">System.object</span><span class="sxs-lookup"><span data-stu-id="daefc-128">System.String</span></span>

## <span data-ttu-id="daefc-129">輸出</span><span class="sxs-lookup"><span data-stu-id="daefc-129">OUTPUTS</span></span>

### <span data-ttu-id="daefc-130">SourceControl 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="daefc-130">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="daefc-131">筆記</span><span class="sxs-lookup"><span data-stu-id="daefc-131">NOTES</span></span>

## <span data-ttu-id="daefc-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="daefc-132">RELATED LINKS</span></span>