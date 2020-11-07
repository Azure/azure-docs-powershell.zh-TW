---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: CC6AF515-2F43-4E1B-BCBB-8DA23F3C6CBD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8687cc00e9ba83c427666e08d0ad46c9aab45e02
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967099"
---
# <span data-ttu-id="743bf-101">Get-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="743bf-101">Get-AzureAutomationVariable</span></span>

## <span data-ttu-id="743bf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="743bf-102">SYNOPSIS</span></span>

<span data-ttu-id="743bf-103">取得自動化變數。</span><span class="sxs-lookup"><span data-stu-id="743bf-103">Gets an Automation variable.</span></span>

## <span data-ttu-id="743bf-104">句法</span><span class="sxs-lookup"><span data-stu-id="743bf-104">SYNTAX</span></span>

### <span data-ttu-id="743bf-105">ByAll (預設) </span><span class="sxs-lookup"><span data-stu-id="743bf-105">ByAll (Default)</span></span>
```
Get-AzureAutomationVariable -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="743bf-106">ByName</span><span class="sxs-lookup"><span data-stu-id="743bf-106">ByName</span></span>
```
Get-AzureAutomationVariable -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="743bf-107">說明</span><span class="sxs-lookup"><span data-stu-id="743bf-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="743bf-108">**AzureAutomationVariable** Cmdlet 會取得一或多個 Microsoft Azure 自動化變數。</span><span class="sxs-lookup"><span data-stu-id="743bf-108">The **Get-AzureAutomationVariable** cmdlet gets one or more Microsoft Azure Automation variables.</span></span>
<span data-ttu-id="743bf-109">根據預設，會傳回所有變數。</span><span class="sxs-lookup"><span data-stu-id="743bf-109">By default, all variables are returned.</span></span>
<span data-ttu-id="743bf-110">若要取得特定變數，請指定其名稱。</span><span class="sxs-lookup"><span data-stu-id="743bf-110">To get a specific variable, specify its name.</span></span>

## <span data-ttu-id="743bf-111">示例</span><span class="sxs-lookup"><span data-stu-id="743bf-111">EXAMPLES</span></span>

### <span data-ttu-id="743bf-112">範例1：取得變數</span><span class="sxs-lookup"><span data-stu-id="743bf-112">Example 1: Get a variable</span></span>
```
PS C:\> $variable = Get-AzureAutomationVariable -AutomationAccountName
PS C:\> "Contoso17" -Name "MyVariable"
PS C:\> $value = $variable.value
```

<span data-ttu-id="743bf-113">這些命令會取得稱為 MyVariable 的自動化變數，並將它的值指派給稱為 $value 的變數。</span><span class="sxs-lookup"><span data-stu-id="743bf-113">These commands get an Automation variable called MyVariable and assign its value to a variable called $value.</span></span>

## <span data-ttu-id="743bf-114">參數</span><span class="sxs-lookup"><span data-stu-id="743bf-114">PARAMETERS</span></span>

### <span data-ttu-id="743bf-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="743bf-115">-AutomationAccountName</span></span>
<span data-ttu-id="743bf-116">指定自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="743bf-116">Specifies the name of the Automation account.</span></span>

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

### <span data-ttu-id="743bf-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="743bf-117">-Name</span></span>
<span data-ttu-id="743bf-118">指定變數的名稱。</span><span class="sxs-lookup"><span data-stu-id="743bf-118">Specifies the name of a variable.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="743bf-119">-設定檔</span><span class="sxs-lookup"><span data-stu-id="743bf-119">-Profile</span></span>
<span data-ttu-id="743bf-120">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="743bf-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="743bf-121">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="743bf-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="743bf-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="743bf-122">CommonParameters</span></span>
<span data-ttu-id="743bf-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="743bf-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="743bf-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="743bf-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="743bf-125">輸入</span><span class="sxs-lookup"><span data-stu-id="743bf-125">INPUTS</span></span>

## <span data-ttu-id="743bf-126">輸出</span><span class="sxs-lookup"><span data-stu-id="743bf-126">OUTPUTS</span></span>

### <span data-ttu-id="743bf-127">[-Azure. 命令]。</span><span class="sxs-lookup"><span data-stu-id="743bf-127">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="743bf-128">筆記</span><span class="sxs-lookup"><span data-stu-id="743bf-128">NOTES</span></span>

## <span data-ttu-id="743bf-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="743bf-129">RELATED LINKS</span></span>

[<span data-ttu-id="743bf-130">新-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="743bf-130">New-AzureAutomationVariable</span></span>](./New-AzureAutomationVariable.md)

[<span data-ttu-id="743bf-131">移除-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="743bf-131">Remove-AzureAutomationVariable</span></span>](./Remove-AzureAutomationVariable.md)

[<span data-ttu-id="743bf-132">Set-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="743bf-132">Set-AzureAutomationVariable</span></span>](./Set-AzureAutomationVariable.md)


