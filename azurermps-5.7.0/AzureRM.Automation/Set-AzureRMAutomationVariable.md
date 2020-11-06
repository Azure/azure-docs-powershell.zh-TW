---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: F344D8D1-5593-4C09-A1CA-37579D2A3A61
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationVariable.md
ms.openlocfilehash: 7426f49d94e82865163320fecd85704aeeff14b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450736"
---
# <span data-ttu-id="b9c33-101">Set-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="b9c33-101">Set-AzureRmAutomationVariable</span></span>

## <span data-ttu-id="b9c33-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b9c33-102">SYNOPSIS</span></span>
<span data-ttu-id="b9c33-103">修改自動化變數。</span><span class="sxs-lookup"><span data-stu-id="b9c33-103">Modifies an Automation variable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9c33-104">句法</span><span class="sxs-lookup"><span data-stu-id="b9c33-104">SYNTAX</span></span>

### <span data-ttu-id="b9c33-105">UpdateVariableValue</span><span class="sxs-lookup"><span data-stu-id="b9c33-105">UpdateVariableValue</span></span>
```
Set-AzureRmAutomationVariable [-Name] <String> -Encrypted <Boolean> -Value <Object>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b9c33-106">UpdateVariableDescription</span><span class="sxs-lookup"><span data-stu-id="b9c33-106">UpdateVariableDescription</span></span>
```
Set-AzureRmAutomationVariable [-Name] <String> -Description <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9c33-107">說明</span><span class="sxs-lookup"><span data-stu-id="b9c33-107">DESCRIPTION</span></span>
<span data-ttu-id="b9c33-108">**AzureRmAutomationVariable** Cmdlet 會修改 Azure 自動化中變數的值或描述。</span><span class="sxs-lookup"><span data-stu-id="b9c33-108">The **Set-AzureRmAutomationVariable** cmdlet modifies the value or description of a variable in Azure Automation.</span></span>
<span data-ttu-id="b9c33-109">若要加密變數，請指定 *加密* 的參數。</span><span class="sxs-lookup"><span data-stu-id="b9c33-109">To encrypt the variable, specify the *Encrypted* parameter.</span></span>
<span data-ttu-id="b9c33-110">建立之後，您就無法修改變數的加密狀態。</span><span class="sxs-lookup"><span data-stu-id="b9c33-110">You cannot modify the encrypted state of a variable after creation.</span></span>
<span data-ttu-id="b9c33-111">針對現有、未加密的變數指定 *加密* 會失敗。</span><span class="sxs-lookup"><span data-stu-id="b9c33-111">Specifying *Encrypted* for an existing, non-encrypted, variable fails.</span></span>

## <span data-ttu-id="b9c33-112">示例</span><span class="sxs-lookup"><span data-stu-id="b9c33-112">EXAMPLES</span></span>

### <span data-ttu-id="b9c33-113">範例1：設定變數的值</span><span class="sxs-lookup"><span data-stu-id="b9c33-113">Example 1: Set the value of a variable</span></span>
```
PS C:\>Set-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -ResourceGroupName "ResourceGroup01" -Value "New Value" -Encrypted $False
```

<span data-ttu-id="b9c33-114">這個命令會針對 Azure 自動化帳戶（名為 Contoso17）中名為 StringVariable22 的變數設定新的值。</span><span class="sxs-lookup"><span data-stu-id="b9c33-114">This command sets a new value for the variable named StringVariable22 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="b9c33-115">參數</span><span class="sxs-lookup"><span data-stu-id="b9c33-115">PARAMETERS</span></span>

### <span data-ttu-id="b9c33-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b9c33-116">-AutomationAccountName</span></span>
<span data-ttu-id="b9c33-117">指定儲存變數的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="b9c33-117">Specifies the name of the Automation account in which the variable is stored.</span></span>

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

### <span data-ttu-id="b9c33-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9c33-118">-DefaultProfile</span></span>
<span data-ttu-id="b9c33-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="b9c33-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b9c33-120">-描述</span><span class="sxs-lookup"><span data-stu-id="b9c33-120">-Description</span></span>
<span data-ttu-id="b9c33-121">指定變數的描述。</span><span class="sxs-lookup"><span data-stu-id="b9c33-121">Specifies a description for the variable.</span></span>

```yaml
Type: String
Parameter Sets: UpdateVariableDescription
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9c33-122">-已加密</span><span class="sxs-lookup"><span data-stu-id="b9c33-122">-Encrypted</span></span>
<span data-ttu-id="b9c33-123">指定 Cmdlet 是否針對儲存空間加密變數的值。</span><span class="sxs-lookup"><span data-stu-id="b9c33-123">Specifies whether cmdlet encrypts the value of the variable for storage.</span></span>

```yaml
Type: Boolean
Parameter Sets: UpdateVariableValue
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9c33-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="b9c33-124">-Name</span></span>
<span data-ttu-id="b9c33-125">指定此 Cmdlet 所修改之變數的名稱。</span><span class="sxs-lookup"><span data-stu-id="b9c33-125">Specifies the name of the variable that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9c33-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9c33-126">-ResourceGroupName</span></span>
<span data-ttu-id="b9c33-127">指定此 Cmdlet 修改變數的資源群組。</span><span class="sxs-lookup"><span data-stu-id="b9c33-127">Specifies the resource group for which this cmdlet modifies a variable.</span></span>

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

### <span data-ttu-id="b9c33-128">-值</span><span class="sxs-lookup"><span data-stu-id="b9c33-128">-Value</span></span>
<span data-ttu-id="b9c33-129">指定變數的值。</span><span class="sxs-lookup"><span data-stu-id="b9c33-129">Specifies a value for the variable.</span></span>

```yaml
Type: Object
Parameter Sets: UpdateVariableValue
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9c33-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9c33-130">CommonParameters</span></span>
<span data-ttu-id="b9c33-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b9c33-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9c33-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b9c33-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9c33-133">輸入</span><span class="sxs-lookup"><span data-stu-id="b9c33-133">INPUTS</span></span>

### <span data-ttu-id="b9c33-134">所有</span><span class="sxs-lookup"><span data-stu-id="b9c33-134">None</span></span>
<span data-ttu-id="b9c33-135">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="b9c33-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b9c33-136">輸出</span><span class="sxs-lookup"><span data-stu-id="b9c33-136">OUTPUTS</span></span>

### <span data-ttu-id="b9c33-137">[-Azure. 命令]。</span><span class="sxs-lookup"><span data-stu-id="b9c33-137">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="b9c33-138">筆記</span><span class="sxs-lookup"><span data-stu-id="b9c33-138">NOTES</span></span>

## <span data-ttu-id="b9c33-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="b9c33-139">RELATED LINKS</span></span>

[<span data-ttu-id="b9c33-140">AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="b9c33-140">Get-AzureRmAutomationVariable</span></span>](./Get-AzureRMAutomationVariable.md)

[<span data-ttu-id="b9c33-141">新-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="b9c33-141">New-AzureRmAutomationVariable</span></span>](./New-AzureRMAutomationVariable.md)

[<span data-ttu-id="b9c33-142">移除-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="b9c33-142">Remove-AzureRmAutomationVariable</span></span>](./Remove-AzureRMAutomationVariable.md)


