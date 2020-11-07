---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 47664B13-5D63-4012-80E1-7982C8FE22E1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 20edd29629cb5dbbfa6f3f538d1530e9c0692e6c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967514"
---
# <span data-ttu-id="b2e2e-101">Set-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="b2e2e-101">Set-AzureAutomationVariable</span></span>

## <span data-ttu-id="b2e2e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b2e2e-102">SYNOPSIS</span></span>

<span data-ttu-id="b2e2e-103">修改自動化變數。</span><span class="sxs-lookup"><span data-stu-id="b2e2e-103">Modifies an Automation variable.</span></span>

## <span data-ttu-id="b2e2e-104">句法</span><span class="sxs-lookup"><span data-stu-id="b2e2e-104">SYNTAX</span></span>

### <span data-ttu-id="b2e2e-105">UpdateVariableValue</span><span class="sxs-lookup"><span data-stu-id="b2e2e-105">UpdateVariableValue</span></span>
```
Set-AzureAutomationVariable -Name <String> -Encrypted <Boolean> -Value <Object> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b2e2e-106">UpdateVariableDescription</span><span class="sxs-lookup"><span data-stu-id="b2e2e-106">UpdateVariableDescription</span></span>
```
Set-AzureAutomationVariable -Name <String> -Description <String> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b2e2e-107">說明</span><span class="sxs-lookup"><span data-stu-id="b2e2e-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="b2e2e-108">**AzureAutomationVariable** Cmdlet 會修改 Microsoft Azure 自動化中變數的值或描述。</span><span class="sxs-lookup"><span data-stu-id="b2e2e-108">The **Set-AzureAutomationVariable** cmdlet modifies the value or description of a variable in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="b2e2e-109">示例</span><span class="sxs-lookup"><span data-stu-id="b2e2e-109">EXAMPLES</span></span>

### <span data-ttu-id="b2e2e-110">範例1：設定變數的值</span><span class="sxs-lookup"><span data-stu-id="b2e2e-110">Example 1: Set the value of a variable</span></span>
```
PS C:\> Set-AzureAutomationVariable -AutomationAccountName "Contoso17" -Name "MyStringVariable" -Value "New Value" -Encrypted $False
```

<span data-ttu-id="b2e2e-111">這個命令會針對 Azure 自動化帳戶（名為 Contoso17）中名為 MyStringVariable 的變數設定新的值。</span><span class="sxs-lookup"><span data-stu-id="b2e2e-111">This command sets a new value for the variable named MyStringVariable in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="b2e2e-112">參數</span><span class="sxs-lookup"><span data-stu-id="b2e2e-112">PARAMETERS</span></span>

### <span data-ttu-id="b2e2e-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b2e2e-113">-AutomationAccountName</span></span>
<span data-ttu-id="b2e2e-114">使用變數指定自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="b2e2e-114">Specifies the name of the Automation account with the variable.</span></span>

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

### <span data-ttu-id="b2e2e-115">-描述</span><span class="sxs-lookup"><span data-stu-id="b2e2e-115">-Description</span></span>
<span data-ttu-id="b2e2e-116">指定變數的描述。</span><span class="sxs-lookup"><span data-stu-id="b2e2e-116">Specifies a description for the variable.</span></span>

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

### <span data-ttu-id="b2e2e-117">-已加密</span><span class="sxs-lookup"><span data-stu-id="b2e2e-117">-Encrypted</span></span>
<span data-ttu-id="b2e2e-118">指出是否要加密變數。</span><span class="sxs-lookup"><span data-stu-id="b2e2e-118">Indicates whether to encrypt the variable.</span></span>

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

### <span data-ttu-id="b2e2e-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="b2e2e-119">-Name</span></span>
<span data-ttu-id="b2e2e-120">指定變數的名稱。</span><span class="sxs-lookup"><span data-stu-id="b2e2e-120">Specifies the name of the variable.</span></span>

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

### <span data-ttu-id="b2e2e-121">-設定檔</span><span class="sxs-lookup"><span data-stu-id="b2e2e-121">-Profile</span></span>
<span data-ttu-id="b2e2e-122">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="b2e2e-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b2e2e-123">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="b2e2e-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b2e2e-124">-值</span><span class="sxs-lookup"><span data-stu-id="b2e2e-124">-Value</span></span>
<span data-ttu-id="b2e2e-125">指定變數的值。</span><span class="sxs-lookup"><span data-stu-id="b2e2e-125">Specifies a value for the variable.</span></span>

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

### <span data-ttu-id="b2e2e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2e2e-126">CommonParameters</span></span>
<span data-ttu-id="b2e2e-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b2e2e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2e2e-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b2e2e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2e2e-129">輸入</span><span class="sxs-lookup"><span data-stu-id="b2e2e-129">INPUTS</span></span>

## <span data-ttu-id="b2e2e-130">輸出</span><span class="sxs-lookup"><span data-stu-id="b2e2e-130">OUTPUTS</span></span>

### <span data-ttu-id="b2e2e-131">[-Azure. 命令]。</span><span class="sxs-lookup"><span data-stu-id="b2e2e-131">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="b2e2e-132">筆記</span><span class="sxs-lookup"><span data-stu-id="b2e2e-132">NOTES</span></span>

## <span data-ttu-id="b2e2e-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="b2e2e-133">RELATED LINKS</span></span>

[<span data-ttu-id="b2e2e-134">AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="b2e2e-134">Get-AzureAutomationVariable</span></span>](./Get-AzureAutomationVariable.md)

[<span data-ttu-id="b2e2e-135">新-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="b2e2e-135">New-AzureAutomationVariable</span></span>](./New-AzureAutomationVariable.md)

[<span data-ttu-id="b2e2e-136">移除-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="b2e2e-136">Remove-AzureAutomationVariable</span></span>](./Remove-AzureAutomationVariable.md)


