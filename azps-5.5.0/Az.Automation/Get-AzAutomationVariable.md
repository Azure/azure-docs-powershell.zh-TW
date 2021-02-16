---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 8FB78A4A-8392-44EE-A907-10FDF756071B
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationVariable.md
ms.openlocfilehash: a8238cf9de2b0b20cb347d16bb74623f6469c03c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100139587"
---
# <span data-ttu-id="23468-101">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="23468-101">Get-AzAutomationVariable</span></span>

## <span data-ttu-id="23468-102">摘要</span><span class="sxs-lookup"><span data-stu-id="23468-102">SYNOPSIS</span></span>
<span data-ttu-id="23468-103">取得自動化變數。</span><span class="sxs-lookup"><span data-stu-id="23468-103">Gets an Automation variable.</span></span>

## <span data-ttu-id="23468-104">句法</span><span class="sxs-lookup"><span data-stu-id="23468-104">SYNTAX</span></span>

### <span data-ttu-id="23468-105">ByAll (預設) </span><span class="sxs-lookup"><span data-stu-id="23468-105">ByAll (Default)</span></span>
```
Get-AzAutomationVariable [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23468-106">ByName</span><span class="sxs-lookup"><span data-stu-id="23468-106">ByName</span></span>
```
Get-AzAutomationVariable [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23468-107">說明</span><span class="sxs-lookup"><span data-stu-id="23468-107">DESCRIPTION</span></span>
<span data-ttu-id="23468-108">**AzAutomationVariable** Cmdlet 會取得一或多個 Azure 自動化變數。</span><span class="sxs-lookup"><span data-stu-id="23468-108">The **Get-AzAutomationVariable** cmdlet gets one or more Azure Automation variables.</span></span>
<span data-ttu-id="23468-109">若要取得特定變數，請指定其名稱。</span><span class="sxs-lookup"><span data-stu-id="23468-109">To get a specific variable, specify its name.</span></span>

## <span data-ttu-id="23468-110">示例</span><span class="sxs-lookup"><span data-stu-id="23468-110">EXAMPLES</span></span>

### <span data-ttu-id="23468-111">範例1：取得變數</span><span class="sxs-lookup"><span data-stu-id="23468-111">Example 1: Get a variable</span></span>
```
PS C:\>$Variable = Get-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "Variable06" -ResourceGroupName "ResourceGroup01"
PS C:\> $Value = $Variable.value
```

<span data-ttu-id="23468-112">第一個命令會在名為 Contoso17 的帳戶中，取得一個名為 Variable06 的自動化變數。</span><span class="sxs-lookup"><span data-stu-id="23468-112">The first command gets an Automation variable named Variable06 in the account named Contoso17.</span></span>
<span data-ttu-id="23468-113">該命令會將該物件儲存在 $Variable 變數中。</span><span class="sxs-lookup"><span data-stu-id="23468-113">The command stores that object in the $Variable variable.</span></span>
<span data-ttu-id="23468-114">第二個命令使用標準點符號來參照 $Variable 的 **value** 屬性。</span><span class="sxs-lookup"><span data-stu-id="23468-114">The second command uses standard dot notation to refer to the **value** property of $Variable.</span></span>
<span data-ttu-id="23468-115">該命令會將值儲存在 $value 變數中。</span><span class="sxs-lookup"><span data-stu-id="23468-115">The command stores the value in the $value variable.</span></span>

## <span data-ttu-id="23468-116">參數</span><span class="sxs-lookup"><span data-stu-id="23468-116">PARAMETERS</span></span>

### <span data-ttu-id="23468-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="23468-117">-AutomationAccountName</span></span>
<span data-ttu-id="23468-118">指定包含此 Cmdlet 所取得之變數的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="23468-118">Specifies the name of the Automation account that contains the variables that this cmdlet gets.</span></span>

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

### <span data-ttu-id="23468-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23468-119">-DefaultProfile</span></span>
<span data-ttu-id="23468-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="23468-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="23468-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="23468-121">-Name</span></span>
<span data-ttu-id="23468-122">指定此 Cmdlet 所取得之變數的名稱。</span><span class="sxs-lookup"><span data-stu-id="23468-122">Specifies the name of a variable that this cmdlet gets.</span></span>

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

### <span data-ttu-id="23468-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23468-123">-ResourceGroupName</span></span>
<span data-ttu-id="23468-124">指定此 Cmdlet 取得其變數的資源群組。</span><span class="sxs-lookup"><span data-stu-id="23468-124">Specifies the resource group for which this cmdlet gets variables.</span></span>

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

### <span data-ttu-id="23468-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23468-125">CommonParameters</span></span>
<span data-ttu-id="23468-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="23468-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23468-127">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="23468-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23468-128">輸入</span><span class="sxs-lookup"><span data-stu-id="23468-128">INPUTS</span></span>

### <span data-ttu-id="23468-129">System.object</span><span class="sxs-lookup"><span data-stu-id="23468-129">System.String</span></span>

## <span data-ttu-id="23468-130">輸出</span><span class="sxs-lookup"><span data-stu-id="23468-130">OUTPUTS</span></span>

### <span data-ttu-id="23468-131">[-Azure. 命令]。</span><span class="sxs-lookup"><span data-stu-id="23468-131">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="23468-132">筆記</span><span class="sxs-lookup"><span data-stu-id="23468-132">NOTES</span></span>

## <span data-ttu-id="23468-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="23468-133">RELATED LINKS</span></span>

[<span data-ttu-id="23468-134">新-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="23468-134">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="23468-135">移除-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="23468-135">Remove-AzAutomationVariable</span></span>](./Remove-AzAutomationVariable.md)

[<span data-ttu-id="23468-136">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="23468-136">Set-AzAutomationVariable</span></span>](./Set-AzAutomationVariable.md)


