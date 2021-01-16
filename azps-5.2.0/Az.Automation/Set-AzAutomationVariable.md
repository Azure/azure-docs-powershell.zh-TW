---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: F344D8D1-5593-4C09-A1CA-37579D2A3A61
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationVariable.md
ms.openlocfilehash: 0ca1e99b68f7cca8d39647357ee81770ea41cefc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98285163"
---
# <span data-ttu-id="0c15c-101">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="0c15c-101">Set-AzAutomationVariable</span></span>

## <span data-ttu-id="0c15c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0c15c-102">SYNOPSIS</span></span>
<span data-ttu-id="0c15c-103">修改自動化變數。</span><span class="sxs-lookup"><span data-stu-id="0c15c-103">Modifies an Automation variable.</span></span>

## <span data-ttu-id="0c15c-104">句法</span><span class="sxs-lookup"><span data-stu-id="0c15c-104">SYNTAX</span></span>

### <span data-ttu-id="0c15c-105">UpdateVariableValue</span><span class="sxs-lookup"><span data-stu-id="0c15c-105">UpdateVariableValue</span></span>
```
Set-AzAutomationVariable [-Name] <String> -Encrypted <Boolean> -Value <Object> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c15c-106">UpdateVariableDescription</span><span class="sxs-lookup"><span data-stu-id="0c15c-106">UpdateVariableDescription</span></span>
```
Set-AzAutomationVariable [-Name] <String> -Description <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c15c-107">說明</span><span class="sxs-lookup"><span data-stu-id="0c15c-107">DESCRIPTION</span></span>
<span data-ttu-id="0c15c-108">**AzAutomationVariable** Cmdlet 會修改 Azure 自動化中變數的值或描述。</span><span class="sxs-lookup"><span data-stu-id="0c15c-108">The **Set-AzAutomationVariable** cmdlet modifies the value or description of a variable in Azure Automation.</span></span>
<span data-ttu-id="0c15c-109">若要加密變數，請指定 *加密* 的參數。</span><span class="sxs-lookup"><span data-stu-id="0c15c-109">To encrypt the variable, specify the *Encrypted* parameter.</span></span>
<span data-ttu-id="0c15c-110">建立之後，您就無法修改變數的加密狀態。</span><span class="sxs-lookup"><span data-stu-id="0c15c-110">You cannot modify the encrypted state of a variable after creation.</span></span>
<span data-ttu-id="0c15c-111">針對現有、未加密的變數指定 *加密* 會失敗。</span><span class="sxs-lookup"><span data-stu-id="0c15c-111">Specifying *Encrypted* for an existing, non-encrypted, variable fails.</span></span>

## <span data-ttu-id="0c15c-112">示例</span><span class="sxs-lookup"><span data-stu-id="0c15c-112">EXAMPLES</span></span>

### <span data-ttu-id="0c15c-113">範例1：設定變數的值</span><span class="sxs-lookup"><span data-stu-id="0c15c-113">Example 1: Set the value of a variable</span></span>
```
PS C:\>Set-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -ResourceGroupName "ResourceGroup01" -Value "New Value" -Encrypted $False
```

<span data-ttu-id="0c15c-114">這個命令會針對 Azure 自動化帳戶（名為 Contoso17）中名為 StringVariable22 的變數設定新的值。</span><span class="sxs-lookup"><span data-stu-id="0c15c-114">This command sets a new value for the variable named StringVariable22 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="0c15c-115">參數</span><span class="sxs-lookup"><span data-stu-id="0c15c-115">PARAMETERS</span></span>

### <span data-ttu-id="0c15c-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0c15c-116">-AutomationAccountName</span></span>
<span data-ttu-id="0c15c-117">指定儲存變數的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="0c15c-117">Specifies the name of the Automation account in which the variable is stored.</span></span>

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

### <span data-ttu-id="0c15c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c15c-118">-DefaultProfile</span></span>
<span data-ttu-id="0c15c-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="0c15c-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0c15c-120">-描述</span><span class="sxs-lookup"><span data-stu-id="0c15c-120">-Description</span></span>
<span data-ttu-id="0c15c-121">指定變數的描述。</span><span class="sxs-lookup"><span data-stu-id="0c15c-121">Specifies a description for the variable.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateVariableDescription
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c15c-122">-已加密</span><span class="sxs-lookup"><span data-stu-id="0c15c-122">-Encrypted</span></span>
<span data-ttu-id="0c15c-123">指定 Cmdlet 是否針對儲存空間加密變數的值。</span><span class="sxs-lookup"><span data-stu-id="0c15c-123">Specifies whether cmdlet encrypts the value of the variable for storage.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: UpdateVariableValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c15c-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="0c15c-124">-Name</span></span>
<span data-ttu-id="0c15c-125">指定此 Cmdlet 所修改之變數的名稱。</span><span class="sxs-lookup"><span data-stu-id="0c15c-125">Specifies the name of the variable that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c15c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c15c-126">-ResourceGroupName</span></span>
<span data-ttu-id="0c15c-127">指定此 Cmdlet 修改變數的資源群組。</span><span class="sxs-lookup"><span data-stu-id="0c15c-127">Specifies the resource group for which this cmdlet modifies a variable.</span></span>

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

### <span data-ttu-id="0c15c-128">-值</span><span class="sxs-lookup"><span data-stu-id="0c15c-128">-Value</span></span>
<span data-ttu-id="0c15c-129">指定變數的值。</span><span class="sxs-lookup"><span data-stu-id="0c15c-129">Specifies a value for the variable.</span></span>

```yaml
Type: System.Object
Parameter Sets: UpdateVariableValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c15c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c15c-130">CommonParameters</span></span>
<span data-ttu-id="0c15c-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0c15c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c15c-132">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0c15c-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c15c-133">輸入</span><span class="sxs-lookup"><span data-stu-id="0c15c-133">INPUTS</span></span>

### <span data-ttu-id="0c15c-134">System.object</span><span class="sxs-lookup"><span data-stu-id="0c15c-134">System.String</span></span>

### <span data-ttu-id="0c15c-135">System.object</span><span class="sxs-lookup"><span data-stu-id="0c15c-135">System.Boolean</span></span>

### <span data-ttu-id="0c15c-136">System.object</span><span class="sxs-lookup"><span data-stu-id="0c15c-136">System.Object</span></span>

## <span data-ttu-id="0c15c-137">輸出</span><span class="sxs-lookup"><span data-stu-id="0c15c-137">OUTPUTS</span></span>

### <span data-ttu-id="0c15c-138">[-Azure. 命令]。</span><span class="sxs-lookup"><span data-stu-id="0c15c-138">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="0c15c-139">筆記</span><span class="sxs-lookup"><span data-stu-id="0c15c-139">NOTES</span></span>

## <span data-ttu-id="0c15c-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="0c15c-140">RELATED LINKS</span></span>

[<span data-ttu-id="0c15c-141">AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="0c15c-141">Get-AzAutomationVariable</span></span>](./Get-AzAutomationVariable.md)

[<span data-ttu-id="0c15c-142">新-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="0c15c-142">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="0c15c-143">移除-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="0c15c-143">Remove-AzAutomationVariable</span></span>](./Remove-AzAutomationVariable.md)


