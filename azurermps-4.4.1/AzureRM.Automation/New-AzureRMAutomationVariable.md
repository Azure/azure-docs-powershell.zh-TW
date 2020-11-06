---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 5AF6F70F-7137-48E2-96ED-2C509042F127
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationVariable.md
ms.openlocfilehash: c2e03cae02c776b69c424ea3ff685a4118ed94bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450908"
---
# <span data-ttu-id="24ab8-101">New-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="24ab8-101">New-AzureRmAutomationVariable</span></span>

## <span data-ttu-id="24ab8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="24ab8-102">SYNOPSIS</span></span>
<span data-ttu-id="24ab8-103">建立自動化變數。</span><span class="sxs-lookup"><span data-stu-id="24ab8-103">Creates an Automation variable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24ab8-104">句法</span><span class="sxs-lookup"><span data-stu-id="24ab8-104">SYNTAX</span></span>

```
New-AzureRmAutomationVariable [-Name] <String> -Encrypted <Boolean> [-Description <String>] [-Value <Object>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="24ab8-105">說明</span><span class="sxs-lookup"><span data-stu-id="24ab8-105">DESCRIPTION</span></span>
<span data-ttu-id="24ab8-106">**新的 AzureRmAutomationVariable** Cmdlet 會在 Azure 自動化中建立一個變數。</span><span class="sxs-lookup"><span data-stu-id="24ab8-106">The **New-AzureRmAutomationVariable** cmdlet creates a variable in Azure Automation.</span></span>
<span data-ttu-id="24ab8-107">若要加密變數，請指定 *加密* 的參數。</span><span class="sxs-lookup"><span data-stu-id="24ab8-107">To encrypt the variable, specify the *Encrypted* parameter.</span></span>
<span data-ttu-id="24ab8-108">建立之後，您就無法修改變數的加密狀態。</span><span class="sxs-lookup"><span data-stu-id="24ab8-108">You cannot modify the encrypted state of a variable after creation.</span></span>

## <span data-ttu-id="24ab8-109">示例</span><span class="sxs-lookup"><span data-stu-id="24ab8-109">EXAMPLES</span></span>

### <span data-ttu-id="24ab8-110">範例1：使用簡單的值建立變數</span><span class="sxs-lookup"><span data-stu-id="24ab8-110">Example 1: Create a variable with a simple value</span></span>
```
PS C:\>New-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Encrypted $False -Value "My String" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="24ab8-111">這個命令會建立一個名為 StringVariable22 的變數，並在名為 Contoso17 的自動化帳戶中使用字串值。</span><span class="sxs-lookup"><span data-stu-id="24ab8-111">This command creates a variable named StringVariable22 with a string value in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="24ab8-112">範例2：建立包含複雜值的變數</span><span class="sxs-lookup"><span data-stu-id="24ab8-112">Example 2: Create a variable with a complex value</span></span>
```
PS C:\>$VirtualMachine = Get-AzureVM -ServiceName "VirtualMachine" -Name "VirtualMachine03"
PS C:\> New-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "ComplexVariable01" -Encrypted $False -Value $VirtualMachine -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="24ab8-113">第一個命令會使用 Get-AzureVM Cmdlet 來取得虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="24ab8-113">The first command gets a virtual machine by using the Get-AzureVM cmdlet.</span></span>
<span data-ttu-id="24ab8-114">該命令會將它儲存在 $VirtualMachine 變數中。</span><span class="sxs-lookup"><span data-stu-id="24ab8-114">The command stores it in the $VirtualMachine variable.</span></span>

<span data-ttu-id="24ab8-115">第二個命令會在名為 Contoso17 的自動化帳戶中，建立一個名為 ComplexVariable01 的變數。</span><span class="sxs-lookup"><span data-stu-id="24ab8-115">The second command creates a variable named ComplexVariable01 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="24ab8-116">這個命令會針對其值使用一個複雜物件（在此例中為 $VirtualMachine 的虛擬機器）。</span><span class="sxs-lookup"><span data-stu-id="24ab8-116">This command uses a complex object for its value, in this case, the virtual machine in $VirtualMachine.</span></span>

## <span data-ttu-id="24ab8-117">參數</span><span class="sxs-lookup"><span data-stu-id="24ab8-117">PARAMETERS</span></span>

### <span data-ttu-id="24ab8-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="24ab8-118">-AutomationAccountName</span></span>
<span data-ttu-id="24ab8-119">指定要儲存變數的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="24ab8-119">Specifies the name of the Automation account in which to store the variable.</span></span>

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

### <span data-ttu-id="24ab8-120">-描述</span><span class="sxs-lookup"><span data-stu-id="24ab8-120">-Description</span></span>
<span data-ttu-id="24ab8-121">指定變數的描述。</span><span class="sxs-lookup"><span data-stu-id="24ab8-121">Specifies a description for the variable.</span></span>

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

### <span data-ttu-id="24ab8-122">-已加密</span><span class="sxs-lookup"><span data-stu-id="24ab8-122">-Encrypted</span></span>
<span data-ttu-id="24ab8-123">指定此 Cmdlet 是否會針對儲存空間加密變數的值。</span><span class="sxs-lookup"><span data-stu-id="24ab8-123">Specifies whether this cmdlet encrypts the value of the variable for storage.</span></span>

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

### <span data-ttu-id="24ab8-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="24ab8-124">-Name</span></span>
<span data-ttu-id="24ab8-125">指定變數的名稱。</span><span class="sxs-lookup"><span data-stu-id="24ab8-125">Specifies a name for the variable.</span></span>

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

### <span data-ttu-id="24ab8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24ab8-126">-ResourceGroupName</span></span>
<span data-ttu-id="24ab8-127">指定此 Cmdlet 為其建立變數的資源群組。</span><span class="sxs-lookup"><span data-stu-id="24ab8-127">Specifies the resource group for which this cmdlet creates a variable.</span></span>

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

### <span data-ttu-id="24ab8-128">-值</span><span class="sxs-lookup"><span data-stu-id="24ab8-128">-Value</span></span>
<span data-ttu-id="24ab8-129">指定變數的值。</span><span class="sxs-lookup"><span data-stu-id="24ab8-129">Specifies a value for the variable.</span></span>

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

### <span data-ttu-id="24ab8-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24ab8-130">-DefaultProfile</span></span>
<span data-ttu-id="24ab8-131">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="24ab8-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24ab8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24ab8-132">CommonParameters</span></span>
<span data-ttu-id="24ab8-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="24ab8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24ab8-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="24ab8-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24ab8-135">輸入</span><span class="sxs-lookup"><span data-stu-id="24ab8-135">INPUTS</span></span>

## <span data-ttu-id="24ab8-136">輸出</span><span class="sxs-lookup"><span data-stu-id="24ab8-136">OUTPUTS</span></span>

### <span data-ttu-id="24ab8-137">[-Azure. 命令]。</span><span class="sxs-lookup"><span data-stu-id="24ab8-137">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="24ab8-138">筆記</span><span class="sxs-lookup"><span data-stu-id="24ab8-138">NOTES</span></span>

## <span data-ttu-id="24ab8-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="24ab8-139">RELATED LINKS</span></span>

[<span data-ttu-id="24ab8-140">AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="24ab8-140">Get-AzureRmAutomationVariable</span></span>](./Get-AzureRMAutomationVariable.md)

[<span data-ttu-id="24ab8-141">移除-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="24ab8-141">Remove-AzureRmAutomationVariable</span></span>](./Remove-AzureRMAutomationVariable.md)

[<span data-ttu-id="24ab8-142">Set-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="24ab8-142">Set-AzureRmAutomationVariable</span></span>](./Set-AzureRMAutomationVariable.md)

