---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 8FB78A4A-8392-44EE-A907-10FDF756071B
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationVariable.md
ms.openlocfilehash: c30e78b21c8f0dbc59e12c0fbecad14cfc93781a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917454"
---
# <span data-ttu-id="a6182-101">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="a6182-101">Get-AzAutomationVariable</span></span>

## <span data-ttu-id="a6182-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a6182-102">SYNOPSIS</span></span>
<span data-ttu-id="a6182-103">獲得自動化變數。</span><span class="sxs-lookup"><span data-stu-id="a6182-103">Gets an Automation variable.</span></span>

## <span data-ttu-id="a6182-104">語法</span><span class="sxs-lookup"><span data-stu-id="a6182-104">SYNTAX</span></span>

### <span data-ttu-id="a6182-105">根據預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="a6182-105">ByAll (Default)</span></span>
```
Get-AzAutomationVariable [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6182-106">ByName</span><span class="sxs-lookup"><span data-stu-id="a6182-106">ByName</span></span>
```
Get-AzAutomationVariable [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6182-107">描述</span><span class="sxs-lookup"><span data-stu-id="a6182-107">DESCRIPTION</span></span>
<span data-ttu-id="a6182-108">**Get-AzAutomationVariable** Cmdlet 會取得一或多個 Azure 自動化變數。</span><span class="sxs-lookup"><span data-stu-id="a6182-108">The **Get-AzAutomationVariable** cmdlet gets one or more Azure Automation variables.</span></span>
<span data-ttu-id="a6182-109">若要取得特定變數，請指定其名稱。</span><span class="sxs-lookup"><span data-stu-id="a6182-109">To get a specific variable, specify its name.</span></span>

## <span data-ttu-id="a6182-110">例子</span><span class="sxs-lookup"><span data-stu-id="a6182-110">EXAMPLES</span></span>

### <span data-ttu-id="a6182-111">範例 1：取得變數</span><span class="sxs-lookup"><span data-stu-id="a6182-111">Example 1: Get a variable</span></span>
```
PS C:\>$Variable = Get-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "Variable06" -ResourceGroupName "ResourceGroup01"
PS C:\> $Value = $Variable.value
```

<span data-ttu-id="a6182-112">第一個命令在名為 Contoso17 的帳戶中，會獲得一個名為 Variable06 的自動化變數。</span><span class="sxs-lookup"><span data-stu-id="a6182-112">The first command gets an Automation variable named Variable06 in the account named Contoso17.</span></span>
<span data-ttu-id="a6182-113">該命令會儲存該物件在$Variable變數中。</span><span class="sxs-lookup"><span data-stu-id="a6182-113">The command stores that object in the $Variable variable.</span></span>
<span data-ttu-id="a6182-114">第二個命令使用標準點標記法來參照 **$Variable。**</span><span class="sxs-lookup"><span data-stu-id="a6182-114">The second command uses standard dot notation to refer to the **value** property of $Variable.</span></span>
<span data-ttu-id="a6182-115">命令會儲存值$value變數。</span><span class="sxs-lookup"><span data-stu-id="a6182-115">The command stores the value in the $value variable.</span></span>

## <span data-ttu-id="a6182-116">參數</span><span class="sxs-lookup"><span data-stu-id="a6182-116">PARAMETERS</span></span>

### <span data-ttu-id="a6182-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a6182-117">-AutomationAccountName</span></span>
<span data-ttu-id="a6182-118">指定包含此 Cmdlet 所獲得變數的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="a6182-118">Specifies the name of the Automation account that contains the variables that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a6182-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6182-119">-DefaultProfile</span></span>
<span data-ttu-id="a6182-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="a6182-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a6182-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="a6182-121">-Name</span></span>
<span data-ttu-id="a6182-122">指定此 Cmdlet 獲得之變數的名稱。</span><span class="sxs-lookup"><span data-stu-id="a6182-122">Specifies the name of a variable that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a6182-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6182-123">-ResourceGroupName</span></span>
<span data-ttu-id="a6182-124">指定此 Cmdlet 會獲得變數的資源群組。</span><span class="sxs-lookup"><span data-stu-id="a6182-124">Specifies the resource group for which this cmdlet gets variables.</span></span>

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

### <span data-ttu-id="a6182-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6182-125">CommonParameters</span></span>
<span data-ttu-id="a6182-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a6182-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6182-127">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="a6182-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6182-128">輸入</span><span class="sxs-lookup"><span data-stu-id="a6182-128">INPUTS</span></span>

### <span data-ttu-id="a6182-129">System.String</span><span class="sxs-lookup"><span data-stu-id="a6182-129">System.String</span></span>

## <span data-ttu-id="a6182-130">輸出</span><span class="sxs-lookup"><span data-stu-id="a6182-130">OUTPUTS</span></span>

### <span data-ttu-id="a6182-131">Microsoft.Azure.Commands.Automation.Model.Variable</span><span class="sxs-lookup"><span data-stu-id="a6182-131">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="a6182-132">筆記</span><span class="sxs-lookup"><span data-stu-id="a6182-132">NOTES</span></span>

## <span data-ttu-id="a6182-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="a6182-133">RELATED LINKS</span></span>

[<span data-ttu-id="a6182-134">New-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="a6182-134">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="a6182-135">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="a6182-135">Remove-AzAutomationVariable</span></span>](./Remove-AzAutomationVariable.md)

[<span data-ttu-id="a6182-136">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="a6182-136">Set-AzAutomationVariable</span></span>](./Set-AzAutomationVariable.md)


