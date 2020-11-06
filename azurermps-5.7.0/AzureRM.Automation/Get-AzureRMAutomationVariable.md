---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 8FB78A4A-8392-44EE-A907-10FDF756071B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationVariable.md
ms.openlocfilehash: 5fccd3f6aa193a3c2cacf39e6b72bccdf440b393
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457499"
---
# <span data-ttu-id="16606-101">Get-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="16606-101">Get-AzureRmAutomationVariable</span></span>

## <span data-ttu-id="16606-102">摘要</span><span class="sxs-lookup"><span data-stu-id="16606-102">SYNOPSIS</span></span>
<span data-ttu-id="16606-103">取得自動化變數。</span><span class="sxs-lookup"><span data-stu-id="16606-103">Gets an Automation variable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16606-104">句法</span><span class="sxs-lookup"><span data-stu-id="16606-104">SYNTAX</span></span>

### <span data-ttu-id="16606-105">ByAll (預設) </span><span class="sxs-lookup"><span data-stu-id="16606-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationVariable [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16606-106">ByName</span><span class="sxs-lookup"><span data-stu-id="16606-106">ByName</span></span>
```
Get-AzureRmAutomationVariable [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16606-107">說明</span><span class="sxs-lookup"><span data-stu-id="16606-107">DESCRIPTION</span></span>
<span data-ttu-id="16606-108">**AzureRmAutomationVariable** Cmdlet 會取得一或多個 Azure 自動化變數。</span><span class="sxs-lookup"><span data-stu-id="16606-108">The **Get-AzureRmAutomationVariable** cmdlet gets one or more Azure Automation variables.</span></span>
<span data-ttu-id="16606-109">若要取得特定變數，請指定其名稱。</span><span class="sxs-lookup"><span data-stu-id="16606-109">To get a specific variable, specify its name.</span></span>

## <span data-ttu-id="16606-110">示例</span><span class="sxs-lookup"><span data-stu-id="16606-110">EXAMPLES</span></span>

### <span data-ttu-id="16606-111">範例1：取得變數</span><span class="sxs-lookup"><span data-stu-id="16606-111">Example 1: Get a variable</span></span>
```
PS C:\>$Variable = Get-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "Variable06" -ResourceGroupName "ResourceGroup01"
PS C:\> $Value = $Variable.value
```

<span data-ttu-id="16606-112">第一個命令會在名為 Contoso17 的帳戶中，取得一個名為 Variable06 的自動化變數。</span><span class="sxs-lookup"><span data-stu-id="16606-112">The first command gets an Automation variable named Variable06 in the account named Contoso17.</span></span>
<span data-ttu-id="16606-113">該命令會將該物件儲存在 $Variable 變數中。</span><span class="sxs-lookup"><span data-stu-id="16606-113">The command stores that object in the $Variable variable.</span></span>

<span data-ttu-id="16606-114">第二個命令使用標準點符號來參照 $Variable 的 **value** 屬性。</span><span class="sxs-lookup"><span data-stu-id="16606-114">The second command uses standard dot notation to refer to the **value** property of $Variable.</span></span>
<span data-ttu-id="16606-115">該命令會將值儲存在 $value 變數中。</span><span class="sxs-lookup"><span data-stu-id="16606-115">The command stores the value in the $value variable.</span></span>

## <span data-ttu-id="16606-116">參數</span><span class="sxs-lookup"><span data-stu-id="16606-116">PARAMETERS</span></span>

### <span data-ttu-id="16606-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="16606-117">-AutomationAccountName</span></span>
<span data-ttu-id="16606-118">指定包含此 Cmdlet 所取得之變數的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="16606-118">Specifies the name of the Automation account that contains the variables that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16606-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16606-119">-DefaultProfile</span></span>
<span data-ttu-id="16606-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="16606-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16606-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="16606-121">-Name</span></span>
<span data-ttu-id="16606-122">指定此 Cmdlet 所取得之變數的名稱。</span><span class="sxs-lookup"><span data-stu-id="16606-122">Specifies the name of a variable that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16606-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16606-123">-ResourceGroupName</span></span>
<span data-ttu-id="16606-124">指定此 Cmdlet 取得其變數的資源群組。</span><span class="sxs-lookup"><span data-stu-id="16606-124">Specifies the resource group for which this cmdlet gets variables.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16606-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16606-125">CommonParameters</span></span>
<span data-ttu-id="16606-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="16606-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16606-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="16606-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16606-128">輸入</span><span class="sxs-lookup"><span data-stu-id="16606-128">INPUTS</span></span>

### <span data-ttu-id="16606-129">所有</span><span class="sxs-lookup"><span data-stu-id="16606-129">None</span></span>
<span data-ttu-id="16606-130">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="16606-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="16606-131">輸出</span><span class="sxs-lookup"><span data-stu-id="16606-131">OUTPUTS</span></span>

### <span data-ttu-id="16606-132">[-Azure. 命令]。</span><span class="sxs-lookup"><span data-stu-id="16606-132">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="16606-133">筆記</span><span class="sxs-lookup"><span data-stu-id="16606-133">NOTES</span></span>

## <span data-ttu-id="16606-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="16606-134">RELATED LINKS</span></span>

[<span data-ttu-id="16606-135">新-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="16606-135">New-AzureRmAutomationVariable</span></span>](./New-AzureRMAutomationVariable.md)

[<span data-ttu-id="16606-136">移除-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="16606-136">Remove-AzureRmAutomationVariable</span></span>](./Remove-AzureRMAutomationVariable.md)

[<span data-ttu-id="16606-137">Set-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="16606-137">Set-AzureRmAutomationVariable</span></span>](./Set-AzureRMAutomationVariable.md)


