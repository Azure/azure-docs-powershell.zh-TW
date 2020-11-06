---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 8FB78A4A-8392-44EE-A907-10FDF756071B
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationVariable.md
ms.openlocfilehash: a430b8a57abf19e036a75039b6bdddb8a7ea0d16
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613761"
---
# <span data-ttu-id="f5879-101">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="f5879-101">Get-AzAutomationVariable</span></span>

## <span data-ttu-id="f5879-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f5879-102">SYNOPSIS</span></span>
<span data-ttu-id="f5879-103">取得自動化變數。</span><span class="sxs-lookup"><span data-stu-id="f5879-103">Gets an Automation variable.</span></span>

## <span data-ttu-id="f5879-104">句法</span><span class="sxs-lookup"><span data-stu-id="f5879-104">SYNTAX</span></span>

### <span data-ttu-id="f5879-105">ByAll (預設) </span><span class="sxs-lookup"><span data-stu-id="f5879-105">ByAll (Default)</span></span>
```
Get-AzAutomationVariable [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f5879-106">ByName</span><span class="sxs-lookup"><span data-stu-id="f5879-106">ByName</span></span>
```
Get-AzAutomationVariable [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5879-107">說明</span><span class="sxs-lookup"><span data-stu-id="f5879-107">DESCRIPTION</span></span>
<span data-ttu-id="f5879-108">**AzAutomationVariable** Cmdlet 會取得一或多個 Azure 自動化變數。</span><span class="sxs-lookup"><span data-stu-id="f5879-108">The **Get-AzAutomationVariable** cmdlet gets one or more Azure Automation variables.</span></span>
<span data-ttu-id="f5879-109">若要取得特定變數，請指定其名稱。</span><span class="sxs-lookup"><span data-stu-id="f5879-109">To get a specific variable, specify its name.</span></span>

## <span data-ttu-id="f5879-110">示例</span><span class="sxs-lookup"><span data-stu-id="f5879-110">EXAMPLES</span></span>

### <span data-ttu-id="f5879-111">範例1：取得變數</span><span class="sxs-lookup"><span data-stu-id="f5879-111">Example 1: Get a variable</span></span>
```
PS C:\>$Variable = Get-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "Variable06" -ResourceGroupName "ResourceGroup01"
PS C:\> $Value = $Variable.value
```

<span data-ttu-id="f5879-112">第一個命令會在名為 Contoso17 的帳戶中，取得一個名為 Variable06 的自動化變數。</span><span class="sxs-lookup"><span data-stu-id="f5879-112">The first command gets an Automation variable named Variable06 in the account named Contoso17.</span></span>
<span data-ttu-id="f5879-113">該命令會將該物件儲存在 $Variable 變數中。</span><span class="sxs-lookup"><span data-stu-id="f5879-113">The command stores that object in the $Variable variable.</span></span>
<span data-ttu-id="f5879-114">第二個命令使用標準點符號來參照 $Variable 的 **value** 屬性。</span><span class="sxs-lookup"><span data-stu-id="f5879-114">The second command uses standard dot notation to refer to the **value** property of $Variable.</span></span>
<span data-ttu-id="f5879-115">該命令會將值儲存在 $value 變數中。</span><span class="sxs-lookup"><span data-stu-id="f5879-115">The command stores the value in the $value variable.</span></span>

## <span data-ttu-id="f5879-116">參數</span><span class="sxs-lookup"><span data-stu-id="f5879-116">PARAMETERS</span></span>

### <span data-ttu-id="f5879-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f5879-117">-AutomationAccountName</span></span>
<span data-ttu-id="f5879-118">指定包含此 Cmdlet 所取得之變數的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="f5879-118">Specifies the name of the Automation account that contains the variables that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f5879-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5879-119">-DefaultProfile</span></span>
<span data-ttu-id="f5879-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="f5879-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f5879-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="f5879-121">-Name</span></span>
<span data-ttu-id="f5879-122">指定此 Cmdlet 所取得之變數的名稱。</span><span class="sxs-lookup"><span data-stu-id="f5879-122">Specifies the name of a variable that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f5879-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5879-123">-ResourceGroupName</span></span>
<span data-ttu-id="f5879-124">指定此 Cmdlet 取得其變數的資源群組。</span><span class="sxs-lookup"><span data-stu-id="f5879-124">Specifies the resource group for which this cmdlet gets variables.</span></span>

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

### <span data-ttu-id="f5879-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5879-125">CommonParameters</span></span>
<span data-ttu-id="f5879-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f5879-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5879-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f5879-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5879-128">輸入</span><span class="sxs-lookup"><span data-stu-id="f5879-128">INPUTS</span></span>

### <span data-ttu-id="f5879-129">System.object</span><span class="sxs-lookup"><span data-stu-id="f5879-129">System.String</span></span>

## <span data-ttu-id="f5879-130">輸出</span><span class="sxs-lookup"><span data-stu-id="f5879-130">OUTPUTS</span></span>

### <span data-ttu-id="f5879-131">[-Azure. 命令]。</span><span class="sxs-lookup"><span data-stu-id="f5879-131">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="f5879-132">筆記</span><span class="sxs-lookup"><span data-stu-id="f5879-132">NOTES</span></span>

## <span data-ttu-id="f5879-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="f5879-133">RELATED LINKS</span></span>

[<span data-ttu-id="f5879-134">新-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="f5879-134">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="f5879-135">移除-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="f5879-135">Remove-AzAutomationVariable</span></span>](./Remove-AzAutomationVariable.md)

[<span data-ttu-id="f5879-136">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="f5879-136">Set-AzAutomationVariable</span></span>](./Set-AzAutomationVariable.md)

