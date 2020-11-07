---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 5AF6F70F-7137-48E2-96ED-2C509042F127
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationVariable.md
ms.openlocfilehash: f60e254e9addf2e7052b010033d9c81ccc6a0a98
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93966396"
---
# <span data-ttu-id="91c0a-101">New-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="91c0a-101">New-AzAutomationVariable</span></span>

## <span data-ttu-id="91c0a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="91c0a-102">SYNOPSIS</span></span>
<span data-ttu-id="91c0a-103">建立自動化變數。</span><span class="sxs-lookup"><span data-stu-id="91c0a-103">Creates an Automation variable.</span></span>

## <span data-ttu-id="91c0a-104">句法</span><span class="sxs-lookup"><span data-stu-id="91c0a-104">SYNTAX</span></span>

```
New-AzAutomationVariable [-Name] <String> -Encrypted <Boolean> [-Description <String>] [-Value <Object>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="91c0a-105">說明</span><span class="sxs-lookup"><span data-stu-id="91c0a-105">DESCRIPTION</span></span>
<span data-ttu-id="91c0a-106">**新的 AzAutomationVariable** Cmdlet 會在 Azure 自動化中建立一個變數。</span><span class="sxs-lookup"><span data-stu-id="91c0a-106">The **New-AzAutomationVariable** cmdlet creates a variable in Azure Automation.</span></span>
<span data-ttu-id="91c0a-107">若要加密變數，請指定 *加密* 的參數。</span><span class="sxs-lookup"><span data-stu-id="91c0a-107">To encrypt the variable, specify the *Encrypted* parameter.</span></span>
<span data-ttu-id="91c0a-108">建立之後，您就無法修改變數的加密狀態。</span><span class="sxs-lookup"><span data-stu-id="91c0a-108">You cannot modify the encrypted state of a variable after creation.</span></span>

## <span data-ttu-id="91c0a-109">示例</span><span class="sxs-lookup"><span data-stu-id="91c0a-109">EXAMPLES</span></span>

### <span data-ttu-id="91c0a-110">範例1：使用簡單的值建立變數</span><span class="sxs-lookup"><span data-stu-id="91c0a-110">Example 1: Create a variable with a simple value</span></span>
```
PS C:\>New-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Encrypted $False -Value "My String" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="91c0a-111">這個命令會建立一個名為 StringVariable22 的變數，並在名為 Contoso17 的自動化帳戶中使用字串值。</span><span class="sxs-lookup"><span data-stu-id="91c0a-111">This command creates a variable named StringVariable22 with a string value in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="91c0a-112">範例2：建立包含複雜值的變數</span><span class="sxs-lookup"><span data-stu-id="91c0a-112">Example 2: Create a variable with a complex value</span></span>
```
PS C:\>$VirtualMachine = Get-AzVM -ServiceName "VirtualMachine" -Name "VirtualMachine03"
PS C:\> New-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "ComplexVariable01" -Encrypted $False -Value $VirtualMachine -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="91c0a-113">第一個命令會使用 Get-AzVM Cmdlet 來取得虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="91c0a-113">The first command gets a virtual machine by using the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="91c0a-114">該命令會將它儲存在 $VirtualMachine 變數中。</span><span class="sxs-lookup"><span data-stu-id="91c0a-114">The command stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="91c0a-115">第二個命令會在名為 Contoso17 的自動化帳戶中，建立一個名為 ComplexVariable01 的變數。</span><span class="sxs-lookup"><span data-stu-id="91c0a-115">The second command creates a variable named ComplexVariable01 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="91c0a-116">這個命令會針對其值使用一個複雜物件（在此例中為 $VirtualMachine 的虛擬機器）。</span><span class="sxs-lookup"><span data-stu-id="91c0a-116">This command uses a complex object for its value, in this case, the virtual machine in $VirtualMachine.</span></span>

## <span data-ttu-id="91c0a-117">參數</span><span class="sxs-lookup"><span data-stu-id="91c0a-117">PARAMETERS</span></span>

### <span data-ttu-id="91c0a-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="91c0a-118">-AutomationAccountName</span></span>
<span data-ttu-id="91c0a-119">指定要儲存變數的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="91c0a-119">Specifies the name of the Automation account in which to store the variable.</span></span>

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

### <span data-ttu-id="91c0a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91c0a-120">-DefaultProfile</span></span>
<span data-ttu-id="91c0a-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="91c0a-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="91c0a-122">-描述</span><span class="sxs-lookup"><span data-stu-id="91c0a-122">-Description</span></span>
<span data-ttu-id="91c0a-123">指定變數的描述。</span><span class="sxs-lookup"><span data-stu-id="91c0a-123">Specifies a description for the variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91c0a-124">-已加密</span><span class="sxs-lookup"><span data-stu-id="91c0a-124">-Encrypted</span></span>
<span data-ttu-id="91c0a-125">指定此 Cmdlet 是否會針對儲存空間加密變數的值。</span><span class="sxs-lookup"><span data-stu-id="91c0a-125">Specifies whether this cmdlet encrypts the value of the variable for storage.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91c0a-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="91c0a-126">-Name</span></span>
<span data-ttu-id="91c0a-127">指定變數的名稱。</span><span class="sxs-lookup"><span data-stu-id="91c0a-127">Specifies a name for the variable.</span></span>

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

### <span data-ttu-id="91c0a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91c0a-128">-ResourceGroupName</span></span>
<span data-ttu-id="91c0a-129">指定此 Cmdlet 為其建立變數的資源群組。</span><span class="sxs-lookup"><span data-stu-id="91c0a-129">Specifies the resource group for which this cmdlet creates a variable.</span></span>

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

### <span data-ttu-id="91c0a-130">-值</span><span class="sxs-lookup"><span data-stu-id="91c0a-130">-Value</span></span>
<span data-ttu-id="91c0a-131">指定變數的值。</span><span class="sxs-lookup"><span data-stu-id="91c0a-131">Specifies a value for the variable.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91c0a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91c0a-132">CommonParameters</span></span>
<span data-ttu-id="91c0a-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="91c0a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91c0a-134">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="91c0a-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91c0a-135">輸入</span><span class="sxs-lookup"><span data-stu-id="91c0a-135">INPUTS</span></span>

### <span data-ttu-id="91c0a-136">System.object</span><span class="sxs-lookup"><span data-stu-id="91c0a-136">System.String</span></span>

### <span data-ttu-id="91c0a-137">System.object</span><span class="sxs-lookup"><span data-stu-id="91c0a-137">System.Boolean</span></span>

### <span data-ttu-id="91c0a-138">System.object</span><span class="sxs-lookup"><span data-stu-id="91c0a-138">System.Object</span></span>

## <span data-ttu-id="91c0a-139">輸出</span><span class="sxs-lookup"><span data-stu-id="91c0a-139">OUTPUTS</span></span>

### <span data-ttu-id="91c0a-140">[-Azure. 命令]。</span><span class="sxs-lookup"><span data-stu-id="91c0a-140">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="91c0a-141">筆記</span><span class="sxs-lookup"><span data-stu-id="91c0a-141">NOTES</span></span>

## <span data-ttu-id="91c0a-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="91c0a-142">RELATED LINKS</span></span>

[<span data-ttu-id="91c0a-143">AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="91c0a-143">Get-AzAutomationVariable</span></span>](./Get-AzAutomationVariable.md)

[<span data-ttu-id="91c0a-144">移除-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="91c0a-144">Remove-AzAutomationVariable</span></span>](./Remove-AzAutomationVariable.md)

[<span data-ttu-id="91c0a-145">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="91c0a-145">Set-AzAutomationVariable</span></span>](./Set-AzAutomationVariable.md)


