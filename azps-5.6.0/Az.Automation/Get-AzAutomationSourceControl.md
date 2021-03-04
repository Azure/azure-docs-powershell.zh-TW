---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControl.md
ms.openlocfilehash: 051eee1c191662e6ca4eb56e34088af651ea69f2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917462"
---
# <span data-ttu-id="80069-101">Get-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="80069-101">Get-AzAutomationSourceControl</span></span>

## <span data-ttu-id="80069-102">簡介</span><span class="sxs-lookup"><span data-stu-id="80069-102">SYNOPSIS</span></span>
<span data-ttu-id="80069-103">獲得 Azure 自動化原始程式碼控制清單。</span><span class="sxs-lookup"><span data-stu-id="80069-103">Gets a list of Azure Automation source controls.</span></span>

## <span data-ttu-id="80069-104">語法</span><span class="sxs-lookup"><span data-stu-id="80069-104">SYNTAX</span></span>

### <span data-ttu-id="80069-105">根據預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="80069-105">ByAll (Default)</span></span>
```
Get-AzAutomationSourceControl [-SourceType <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80069-106">ByName</span><span class="sxs-lookup"><span data-stu-id="80069-106">ByName</span></span>
```
Get-AzAutomationSourceControl -Name <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80069-107">描述</span><span class="sxs-lookup"><span data-stu-id="80069-107">DESCRIPTION</span></span>
<span data-ttu-id="80069-108">Cmdlet Get-AzAutomationSourceControl自動化原始程式碼控制項。</span><span class="sxs-lookup"><span data-stu-id="80069-108">The Get-AzAutomationSourceControl cmdlet gets Automation source controls.</span></span>
<span data-ttu-id="80069-109">若要取得特定的原始程式碼管理，請指定其名稱。</span><span class="sxs-lookup"><span data-stu-id="80069-109">To get a specific source control, specify its name.</span></span>

## <span data-ttu-id="80069-110">例子</span><span class="sxs-lookup"><span data-stu-id="80069-110">EXAMPLES</span></span>

### <span data-ttu-id="80069-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="80069-111">Example 1</span></span>
<span data-ttu-id="80069-112">此命令在名為 devAccount 的帳戶中，會獲得一個名為 VSTSNative 的自動化原始程式碼。</span><span class="sxs-lookup"><span data-stu-id="80069-112">This command gets an Automation source control named VSTSNative in the account named devAccount.</span></span>


```powershell
PS C:\> Get-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name "VSTSNative" 


Name            SourceType Branch FolderPath  AutoSync PublishRunbook RepoUrl
----            ---------- ------ ----------  -------- -------------- -------
VSTSNative      VsoTfvc           /MyRunbooks False    True           https://contoso.visualstudio.com/_git/Fin...
```

## <span data-ttu-id="80069-113">參數</span><span class="sxs-lookup"><span data-stu-id="80069-113">PARAMETERS</span></span>

### <span data-ttu-id="80069-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="80069-114">-AutomationAccountName</span></span>
<span data-ttu-id="80069-115">自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="80069-115">The automation account name.</span></span>

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

### <span data-ttu-id="80069-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80069-116">-DefaultProfile</span></span>
<span data-ttu-id="80069-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="80069-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80069-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="80069-118">-Name</span></span>
<span data-ttu-id="80069-119">原始程式碼管理名稱。</span><span class="sxs-lookup"><span data-stu-id="80069-119">The source control name.</span></span>

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

### <span data-ttu-id="80069-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80069-120">-ResourceGroupName</span></span>
<span data-ttu-id="80069-121">資源組名。</span><span class="sxs-lookup"><span data-stu-id="80069-121">The resource group name.</span></span>

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

### <span data-ttu-id="80069-122">-SourceType</span><span class="sxs-lookup"><span data-stu-id="80069-122">-SourceType</span></span>
<span data-ttu-id="80069-123">原始程式碼管理類型。</span><span class="sxs-lookup"><span data-stu-id="80069-123">The source control type.</span></span>

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

### <span data-ttu-id="80069-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80069-124">CommonParameters</span></span>
<span data-ttu-id="80069-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="80069-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80069-126">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="80069-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80069-127">輸入</span><span class="sxs-lookup"><span data-stu-id="80069-127">INPUTS</span></span>

### <span data-ttu-id="80069-128">System.String</span><span class="sxs-lookup"><span data-stu-id="80069-128">System.String</span></span>

## <span data-ttu-id="80069-129">輸出</span><span class="sxs-lookup"><span data-stu-id="80069-129">OUTPUTS</span></span>

### <span data-ttu-id="80069-130">Microsoft.Azure.Commands.Automation.Model.SourceControl</span><span class="sxs-lookup"><span data-stu-id="80069-130">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="80069-131">筆記</span><span class="sxs-lookup"><span data-stu-id="80069-131">NOTES</span></span>

## <span data-ttu-id="80069-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="80069-132">RELATED LINKS</span></span>
