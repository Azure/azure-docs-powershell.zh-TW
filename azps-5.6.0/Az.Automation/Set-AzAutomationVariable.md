---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: F344D8D1-5593-4C09-A1CA-37579D2A3A61
online version: https://docs.microsoft.com/powershell/module/az.automation/set-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationVariable.md
ms.openlocfilehash: ff83049e6afec5b0a6712aef2622bd9cbe0110c9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915625"
---
# <span data-ttu-id="b3618-101">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="b3618-101">Set-AzAutomationVariable</span></span>

## <span data-ttu-id="b3618-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b3618-102">SYNOPSIS</span></span>
<span data-ttu-id="b3618-103">修改自動化變數。</span><span class="sxs-lookup"><span data-stu-id="b3618-103">Modifies an Automation variable.</span></span>

## <span data-ttu-id="b3618-104">語法</span><span class="sxs-lookup"><span data-stu-id="b3618-104">SYNTAX</span></span>

### <span data-ttu-id="b3618-105">UpdateVariableValue</span><span class="sxs-lookup"><span data-stu-id="b3618-105">UpdateVariableValue</span></span>
```
Set-AzAutomationVariable [-Name] <String> -Encrypted <Boolean> -Value <Object> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3618-106">UpdateVariableDescription</span><span class="sxs-lookup"><span data-stu-id="b3618-106">UpdateVariableDescription</span></span>
```
Set-AzAutomationVariable [-Name] <String> -Description <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3618-107">描述</span><span class="sxs-lookup"><span data-stu-id="b3618-107">DESCRIPTION</span></span>
<span data-ttu-id="b3618-108">**Set-AzAutomationVariable** Cmdlet 會修改 Azure Automation 中變數的值或描述。</span><span class="sxs-lookup"><span data-stu-id="b3618-108">The **Set-AzAutomationVariable** cmdlet modifies the value or description of a variable in Azure Automation.</span></span>
<span data-ttu-id="b3618-109">若要加密變數，請指定 *Encrypted* 參數。</span><span class="sxs-lookup"><span data-stu-id="b3618-109">To encrypt the variable, specify the *Encrypted* parameter.</span></span>
<span data-ttu-id="b3618-110">您無法在建立後修改變數的加密狀態。</span><span class="sxs-lookup"><span data-stu-id="b3618-110">You cannot modify the encrypted state of a variable after creation.</span></span>
<span data-ttu-id="b3618-111">針對 *現有、* 非加密的變數指定加密會失敗。</span><span class="sxs-lookup"><span data-stu-id="b3618-111">Specifying *Encrypted* for an existing, non-encrypted, variable fails.</span></span>

## <span data-ttu-id="b3618-112">例子</span><span class="sxs-lookup"><span data-stu-id="b3618-112">EXAMPLES</span></span>

### <span data-ttu-id="b3618-113">範例 1：設定變數的值</span><span class="sxs-lookup"><span data-stu-id="b3618-113">Example 1: Set the value of a variable</span></span>
```
PS C:\>Set-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -ResourceGroupName "ResourceGroup01" -Value "New Value" -Encrypted $False
```

<span data-ttu-id="b3618-114">此命令會針對 Azure Automation 帳戶中名為 Contoso17 的 StringVariable22 變數設定新值。</span><span class="sxs-lookup"><span data-stu-id="b3618-114">This command sets a new value for the variable named StringVariable22 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="b3618-115">參數</span><span class="sxs-lookup"><span data-stu-id="b3618-115">PARAMETERS</span></span>

### <span data-ttu-id="b3618-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b3618-116">-AutomationAccountName</span></span>
<span data-ttu-id="b3618-117">指定儲存變數的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="b3618-117">Specifies the name of the Automation account in which the variable is stored.</span></span>

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

### <span data-ttu-id="b3618-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3618-118">-DefaultProfile</span></span>
<span data-ttu-id="b3618-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="b3618-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b3618-120">-描述</span><span class="sxs-lookup"><span data-stu-id="b3618-120">-Description</span></span>
<span data-ttu-id="b3618-121">指定變數的描述。</span><span class="sxs-lookup"><span data-stu-id="b3618-121">Specifies a description for the variable.</span></span>

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

### <span data-ttu-id="b3618-122">-加密</span><span class="sxs-lookup"><span data-stu-id="b3618-122">-Encrypted</span></span>
<span data-ttu-id="b3618-123">指定 Cmdlet 是否要加密儲存變數的值。</span><span class="sxs-lookup"><span data-stu-id="b3618-123">Specifies whether cmdlet encrypts the value of the variable for storage.</span></span>

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

### <span data-ttu-id="b3618-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="b3618-124">-Name</span></span>
<span data-ttu-id="b3618-125">指定此 Cmdlet 修改的變數名稱。</span><span class="sxs-lookup"><span data-stu-id="b3618-125">Specifies the name of the variable that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="b3618-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3618-126">-ResourceGroupName</span></span>
<span data-ttu-id="b3618-127">指定此 Cmdlet 修改變數的資源群組。</span><span class="sxs-lookup"><span data-stu-id="b3618-127">Specifies the resource group for which this cmdlet modifies a variable.</span></span>

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

### <span data-ttu-id="b3618-128">-值</span><span class="sxs-lookup"><span data-stu-id="b3618-128">-Value</span></span>
<span data-ttu-id="b3618-129">指定變數的值。</span><span class="sxs-lookup"><span data-stu-id="b3618-129">Specifies a value for the variable.</span></span>

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

### <span data-ttu-id="b3618-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3618-130">CommonParameters</span></span>
<span data-ttu-id="b3618-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b3618-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3618-132">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="b3618-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3618-133">輸入</span><span class="sxs-lookup"><span data-stu-id="b3618-133">INPUTS</span></span>

### <span data-ttu-id="b3618-134">System.String</span><span class="sxs-lookup"><span data-stu-id="b3618-134">System.String</span></span>

### <span data-ttu-id="b3618-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b3618-135">System.Boolean</span></span>

### <span data-ttu-id="b3618-136">System.Object</span><span class="sxs-lookup"><span data-stu-id="b3618-136">System.Object</span></span>

## <span data-ttu-id="b3618-137">輸出</span><span class="sxs-lookup"><span data-stu-id="b3618-137">OUTPUTS</span></span>

### <span data-ttu-id="b3618-138">Microsoft.Azure.Commands.Automation.Model.Variable</span><span class="sxs-lookup"><span data-stu-id="b3618-138">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="b3618-139">筆記</span><span class="sxs-lookup"><span data-stu-id="b3618-139">NOTES</span></span>

## <span data-ttu-id="b3618-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="b3618-140">RELATED LINKS</span></span>

[<span data-ttu-id="b3618-141">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="b3618-141">Get-AzAutomationVariable</span></span>](./Get-AzAutomationVariable.md)

[<span data-ttu-id="b3618-142">New-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="b3618-142">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="b3618-143">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="b3618-143">Remove-AzAutomationVariable</span></span>](./Remove-AzAutomationVariable.md)


