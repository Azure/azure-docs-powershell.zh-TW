---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: D88C6B17-5D0E-4E23-9C5C-DB38DED9061C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1518c351a67c84e6dacafd1fa8a394051f3bfeac
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967377"
---
# <span data-ttu-id="4b8fc-101">New-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="4b8fc-101">New-AzureAutomationVariable</span></span>

## <span data-ttu-id="4b8fc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4b8fc-102">SYNOPSIS</span></span>

<span data-ttu-id="4b8fc-103">建立自動化變數。</span><span class="sxs-lookup"><span data-stu-id="4b8fc-103">Creates an Automation variable.</span></span>

## <span data-ttu-id="4b8fc-104">句法</span><span class="sxs-lookup"><span data-stu-id="4b8fc-104">SYNTAX</span></span>

```
New-AzureAutomationVariable -Name <String> -Encrypted <Boolean> [-Description <String>] [-Value <Object>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4b8fc-105">說明</span><span class="sxs-lookup"><span data-stu-id="4b8fc-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="4b8fc-106">**新的 AzureAutomationVariable** Cmdlet 會在 Microsoft Azure 自動化中建立一個變數。</span><span class="sxs-lookup"><span data-stu-id="4b8fc-106">The **New-AzureAutomationVariable** cmdlet creates a variable in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="4b8fc-107">示例</span><span class="sxs-lookup"><span data-stu-id="4b8fc-107">EXAMPLES</span></span>

### <span data-ttu-id="4b8fc-108">範例1：使用簡單的值建立新的變數</span><span class="sxs-lookup"><span data-stu-id="4b8fc-108">Example 1: Create a new variable with a simple value</span></span>
```
PS C:\> New-AzureAutomationVariable -AutomationAccountName "Contoso17" -Name "MyStringVariable" -Encrypted $False -Value "My String"
```

<span data-ttu-id="4b8fc-109">這個命令會使用 Azure 自動化帳戶（名為 Contoso17）中的字串值來建立名為 MyStringVariable 的新變數。</span><span class="sxs-lookup"><span data-stu-id="4b8fc-109">This command creates a new variable named MyStringVariable with a string value in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="4b8fc-110">範例2：建立含複雜值的新變數</span><span class="sxs-lookup"><span data-stu-id="4b8fc-110">Example 2: Create a new variable with a complex value</span></span>
```
PS C:\> $vm = Get-AzureVM -ServiceName "MyVM" -Name "MyVM"
PS C:\> New-AzureAutomationVariable -AutomationAccountName "Contoso17" -Name "MyComplexVariable" -Encrypted $False -Value $vm
```

<span data-ttu-id="4b8fc-111">這些命令會在名為 Contoso17 的自動化帳戶中，建立一個名為 MyComplexVariable 的新變數。</span><span class="sxs-lookup"><span data-stu-id="4b8fc-111">These commands create a new variable called MyComplexVariable in the Automation account named Contoso17.</span></span>
<span data-ttu-id="4b8fc-112">在此情況下，會將複雜物件用於其值（在此例中為虛擬電腦物件）。</span><span class="sxs-lookup"><span data-stu-id="4b8fc-112">A complex object is used for its value, in this case a virtual machine object.</span></span>

## <span data-ttu-id="4b8fc-113">參數</span><span class="sxs-lookup"><span data-stu-id="4b8fc-113">PARAMETERS</span></span>

### <span data-ttu-id="4b8fc-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4b8fc-114">-AutomationAccountName</span></span>
<span data-ttu-id="4b8fc-115">指定將儲存變數的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="4b8fc-115">Specifies the name of the Automation account the variable will be stored in.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b8fc-116">-描述</span><span class="sxs-lookup"><span data-stu-id="4b8fc-116">-Description</span></span>
<span data-ttu-id="4b8fc-117">指定變數的描述。</span><span class="sxs-lookup"><span data-stu-id="4b8fc-117">Specifies a description for the variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b8fc-118">-已加密</span><span class="sxs-lookup"><span data-stu-id="4b8fc-118">-Encrypted</span></span>
<span data-ttu-id="4b8fc-119">指示是否應將變數的值儲存為已加密。</span><span class="sxs-lookup"><span data-stu-id="4b8fc-119">Indicates whether the value of the variable should be stored encrypted.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b8fc-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="4b8fc-120">-Name</span></span>
<span data-ttu-id="4b8fc-121">指定變數的名稱。</span><span class="sxs-lookup"><span data-stu-id="4b8fc-121">Specifies a name for the variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b8fc-122">-設定檔</span><span class="sxs-lookup"><span data-stu-id="4b8fc-122">-Profile</span></span>
<span data-ttu-id="4b8fc-123">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="4b8fc-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4b8fc-124">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="4b8fc-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b8fc-125">-值</span><span class="sxs-lookup"><span data-stu-id="4b8fc-125">-Value</span></span>
<span data-ttu-id="4b8fc-126">指定要儲存在變數中的值。</span><span class="sxs-lookup"><span data-stu-id="4b8fc-126">Specifies a value to store in the variable.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b8fc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b8fc-127">CommonParameters</span></span>
<span data-ttu-id="4b8fc-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4b8fc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b8fc-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4b8fc-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b8fc-130">輸入</span><span class="sxs-lookup"><span data-stu-id="4b8fc-130">INPUTS</span></span>

## <span data-ttu-id="4b8fc-131">輸出</span><span class="sxs-lookup"><span data-stu-id="4b8fc-131">OUTPUTS</span></span>

### <span data-ttu-id="4b8fc-132">[-Azure. 命令]。</span><span class="sxs-lookup"><span data-stu-id="4b8fc-132">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="4b8fc-133">筆記</span><span class="sxs-lookup"><span data-stu-id="4b8fc-133">NOTES</span></span>

## <span data-ttu-id="4b8fc-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="4b8fc-134">RELATED LINKS</span></span>

[<span data-ttu-id="4b8fc-135">AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="4b8fc-135">Get-AzureAutomationVariable</span></span>](./Get-AzureAutomationVariable.md)

[<span data-ttu-id="4b8fc-136">移除-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="4b8fc-136">Remove-AzureAutomationVariable</span></span>](./Remove-AzureAutomationVariable.md)

[<span data-ttu-id="4b8fc-137">Set-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="4b8fc-137">Set-AzureAutomationVariable</span></span>](./Set-AzureAutomationVariable.md)


