---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A73B388A-E859-40D3-BA63-0E231CF1E81D
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationModule.md
ms.openlocfilehash: 978e1bf2e826e576745748c43249bf8257f129cc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917498"
---
# <span data-ttu-id="98668-101">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="98668-101">Get-AzAutomationModule</span></span>

## <span data-ttu-id="98668-102">簡介</span><span class="sxs-lookup"><span data-stu-id="98668-102">SYNOPSIS</span></span>
<span data-ttu-id="98668-103">從自動化中獲得模組的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="98668-103">Gets metadata for modules from Automation.</span></span>

## <span data-ttu-id="98668-104">語法</span><span class="sxs-lookup"><span data-stu-id="98668-104">SYNTAX</span></span>

### <span data-ttu-id="98668-105">根據預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="98668-105">ByAll (Default)</span></span>
```
Get-AzAutomationModule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98668-106">ByName</span><span class="sxs-lookup"><span data-stu-id="98668-106">ByName</span></span>
```
Get-AzAutomationModule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98668-107">描述</span><span class="sxs-lookup"><span data-stu-id="98668-107">DESCRIPTION</span></span>
<span data-ttu-id="98668-108">**Get-AzAutomationModule Cmdlet** 會從 Azure Automation 取得模組的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="98668-108">The **Get-AzAutomationModule** cmdlet gets metadata for modules from Azure Automation.</span></span>

## <span data-ttu-id="98668-109">例子</span><span class="sxs-lookup"><span data-stu-id="98668-109">EXAMPLES</span></span>

### <span data-ttu-id="98668-110">範例 1：取得所有模組</span><span class="sxs-lookup"><span data-stu-id="98668-110">Example 1: Get all modules</span></span>
```
PS C:\>Get-AzAutomationModule -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="98668-111">此命令會獲得自動化帳戶中名為 Contoso17 的所有模組。</span><span class="sxs-lookup"><span data-stu-id="98668-111">This command gets all modules in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="98668-112">範例 2：取得模組</span><span class="sxs-lookup"><span data-stu-id="98668-112">Example 2: Get a module</span></span>
```
PS C:\>Get-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="98668-113">此命令在自動化帳戶名為 Contoso17 中，會獲得一個名為 ContosoModule 的模組。</span><span class="sxs-lookup"><span data-stu-id="98668-113">This command gets a module named ContosoModule in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="98668-114">參數</span><span class="sxs-lookup"><span data-stu-id="98668-114">PARAMETERS</span></span>

### <span data-ttu-id="98668-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="98668-115">-AutomationAccountName</span></span>
<span data-ttu-id="98668-116">指定此 Cmdlet 會獲得模組中繼資料的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="98668-116">Specifies the name of the Automation account for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="98668-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98668-117">-DefaultProfile</span></span>
<span data-ttu-id="98668-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="98668-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="98668-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="98668-119">-Name</span></span>
<span data-ttu-id="98668-120">指定此 Cmdlet 會獲得中繼資料的模組名稱。</span><span class="sxs-lookup"><span data-stu-id="98668-120">Specifies the name of the module for which this cmdlet gets metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98668-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98668-121">-ResourceGroupName</span></span>
<span data-ttu-id="98668-122">指定此 Cmdlet 會獲得模組中繼資料的資源組名。</span><span class="sxs-lookup"><span data-stu-id="98668-122">Specifies the name of a resource group for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="98668-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98668-123">CommonParameters</span></span>
<span data-ttu-id="98668-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="98668-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98668-125">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="98668-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98668-126">輸入</span><span class="sxs-lookup"><span data-stu-id="98668-126">INPUTS</span></span>

### <span data-ttu-id="98668-127">System.String</span><span class="sxs-lookup"><span data-stu-id="98668-127">System.String</span></span>

## <span data-ttu-id="98668-128">輸出</span><span class="sxs-lookup"><span data-stu-id="98668-128">OUTPUTS</span></span>

### <span data-ttu-id="98668-129">Microsoft.Azure.Commands.Automation.Model.Module</span><span class="sxs-lookup"><span data-stu-id="98668-129">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="98668-130">筆記</span><span class="sxs-lookup"><span data-stu-id="98668-130">NOTES</span></span>

## <span data-ttu-id="98668-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="98668-131">RELATED LINKS</span></span>

[<span data-ttu-id="98668-132">New-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="98668-132">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="98668-133">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="98668-133">Remove-AzAutomationModule</span></span>](./Remove-AzAutomationModule.md)

[<span data-ttu-id="98668-134">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="98668-134">Set-AzAutomationModule</span></span>](./Set-AzAutomationModule.md)


