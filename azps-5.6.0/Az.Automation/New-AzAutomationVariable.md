---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 5AF6F70F-7137-48E2-96ED-2C509042F127
online version: https://docs.microsoft.com/powershell/module/az.automation/new-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationVariable.md
ms.openlocfilehash: d5058a3741bfaf598793f81ae030541d26aa4aa5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903042"
---
# <span data-ttu-id="de36d-101">New-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="de36d-101">New-AzAutomationVariable</span></span>

## <span data-ttu-id="de36d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="de36d-102">SYNOPSIS</span></span>
<span data-ttu-id="de36d-103">建立自動化變數。</span><span class="sxs-lookup"><span data-stu-id="de36d-103">Creates an Automation variable.</span></span>

## <span data-ttu-id="de36d-104">語法</span><span class="sxs-lookup"><span data-stu-id="de36d-104">SYNTAX</span></span>

```
New-AzAutomationVariable [-Name] <String> -Encrypted <Boolean> [-Description <String>] [-Value <Object>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="de36d-105">描述</span><span class="sxs-lookup"><span data-stu-id="de36d-105">DESCRIPTION</span></span>
<span data-ttu-id="de36d-106">**New-AzAutomationVariable** Cmdlet 在 Azure Automation 中建立變數。</span><span class="sxs-lookup"><span data-stu-id="de36d-106">The **New-AzAutomationVariable** cmdlet creates a variable in Azure Automation.</span></span>
<span data-ttu-id="de36d-107">若要加密變數，請指定 *Encrypted* 參數。</span><span class="sxs-lookup"><span data-stu-id="de36d-107">To encrypt the variable, specify the *Encrypted* parameter.</span></span>
<span data-ttu-id="de36d-108">您無法在建立後修改變數的加密狀態。</span><span class="sxs-lookup"><span data-stu-id="de36d-108">You cannot modify the encrypted state of a variable after creation.</span></span>

## <span data-ttu-id="de36d-109">例子</span><span class="sxs-lookup"><span data-stu-id="de36d-109">EXAMPLES</span></span>

### <span data-ttu-id="de36d-110">範例 1：使用簡單的值建立變數</span><span class="sxs-lookup"><span data-stu-id="de36d-110">Example 1: Create a variable with a simple value</span></span>
```
PS C:\>New-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Encrypted $False -Value "My String" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="de36d-111">此命令會建立一個名為 StringVariable22 的變數，其字串值在自動化帳戶中名為 Contoso17。</span><span class="sxs-lookup"><span data-stu-id="de36d-111">This command creates a variable named StringVariable22 with a string value in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="de36d-112">範例 2：建立具有複雜值的變數</span><span class="sxs-lookup"><span data-stu-id="de36d-112">Example 2: Create a variable with a complex value</span></span>
```
PS C:\>$VirtualMachine = Get-AzVM -ServiceName "VirtualMachine" -Name "VirtualMachine03"
PS C:\> New-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "ComplexVariable01" -Encrypted $False -Value $VirtualMachine -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="de36d-113">第一個命令會使用 Get-AzVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="de36d-113">The first command gets a virtual machine by using the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="de36d-114">命令會儲存在$VirtualMachine變數中。</span><span class="sxs-lookup"><span data-stu-id="de36d-114">The command stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="de36d-115">第二個命令在自動化帳戶中建立名為 Contoso17 的 ComplexVariable01 變數。</span><span class="sxs-lookup"><span data-stu-id="de36d-115">The second command creates a variable named ComplexVariable01 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="de36d-116">此命令會使用複雜的物件來表示其值，在此例中為 $VirtualMachine。</span><span class="sxs-lookup"><span data-stu-id="de36d-116">This command uses a complex object for its value, in this case, the virtual machine in $VirtualMachine.</span></span>

## <span data-ttu-id="de36d-117">參數</span><span class="sxs-lookup"><span data-stu-id="de36d-117">PARAMETERS</span></span>

### <span data-ttu-id="de36d-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="de36d-118">-AutomationAccountName</span></span>
<span data-ttu-id="de36d-119">指定儲存變數的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="de36d-119">Specifies the name of the Automation account in which to store the variable.</span></span>

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

### <span data-ttu-id="de36d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de36d-120">-DefaultProfile</span></span>
<span data-ttu-id="de36d-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="de36d-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="de36d-122">-描述</span><span class="sxs-lookup"><span data-stu-id="de36d-122">-Description</span></span>
<span data-ttu-id="de36d-123">指定變數的描述。</span><span class="sxs-lookup"><span data-stu-id="de36d-123">Specifies a description for the variable.</span></span>

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

### <span data-ttu-id="de36d-124">-加密</span><span class="sxs-lookup"><span data-stu-id="de36d-124">-Encrypted</span></span>
<span data-ttu-id="de36d-125">指定此 Cmdlet 是否會加密儲存變數的值。</span><span class="sxs-lookup"><span data-stu-id="de36d-125">Specifies whether this cmdlet encrypts the value of the variable for storage.</span></span>

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

### <span data-ttu-id="de36d-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="de36d-126">-Name</span></span>
<span data-ttu-id="de36d-127">指定變數的名稱。</span><span class="sxs-lookup"><span data-stu-id="de36d-127">Specifies a name for the variable.</span></span>

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

### <span data-ttu-id="de36d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de36d-128">-ResourceGroupName</span></span>
<span data-ttu-id="de36d-129">指定此 Cmdlet 建立變數的資源群組。</span><span class="sxs-lookup"><span data-stu-id="de36d-129">Specifies the resource group for which this cmdlet creates a variable.</span></span>

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

### <span data-ttu-id="de36d-130">-值</span><span class="sxs-lookup"><span data-stu-id="de36d-130">-Value</span></span>
<span data-ttu-id="de36d-131">指定變數的值。</span><span class="sxs-lookup"><span data-stu-id="de36d-131">Specifies a value for the variable.</span></span>

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

### <span data-ttu-id="de36d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de36d-132">CommonParameters</span></span>
<span data-ttu-id="de36d-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="de36d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de36d-134">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="de36d-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de36d-135">輸入</span><span class="sxs-lookup"><span data-stu-id="de36d-135">INPUTS</span></span>

### <span data-ttu-id="de36d-136">System.String</span><span class="sxs-lookup"><span data-stu-id="de36d-136">System.String</span></span>

### <span data-ttu-id="de36d-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="de36d-137">System.Boolean</span></span>

### <span data-ttu-id="de36d-138">System.Object</span><span class="sxs-lookup"><span data-stu-id="de36d-138">System.Object</span></span>

## <span data-ttu-id="de36d-139">輸出</span><span class="sxs-lookup"><span data-stu-id="de36d-139">OUTPUTS</span></span>

### <span data-ttu-id="de36d-140">Microsoft.Azure.Commands.Automation.Model.Variable</span><span class="sxs-lookup"><span data-stu-id="de36d-140">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="de36d-141">筆記</span><span class="sxs-lookup"><span data-stu-id="de36d-141">NOTES</span></span>

## <span data-ttu-id="de36d-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="de36d-142">RELATED LINKS</span></span>

[<span data-ttu-id="de36d-143">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="de36d-143">Get-AzAutomationVariable</span></span>](./Get-AzAutomationVariable.md)

[<span data-ttu-id="de36d-144">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="de36d-144">Remove-AzAutomationVariable</span></span>](./Remove-AzAutomationVariable.md)

[<span data-ttu-id="de36d-145">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="de36d-145">Set-AzAutomationVariable</span></span>](./Set-AzAutomationVariable.md)


