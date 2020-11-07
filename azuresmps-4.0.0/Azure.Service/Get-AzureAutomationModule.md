---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 73F90276-FABD-414A-B29D-83F371C1ED21
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0544b4d5fafcb388b65271e736f43a15f02980c5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967814"
---
# <span data-ttu-id="72323-101">Get-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="72323-101">Get-AzureAutomationModule</span></span>

## <span data-ttu-id="72323-102">摘要</span><span class="sxs-lookup"><span data-stu-id="72323-102">SYNOPSIS</span></span>

<span data-ttu-id="72323-103">取得 Azure 自動化模組。</span><span class="sxs-lookup"><span data-stu-id="72323-103">Get an Azure Automation module.</span></span>

## <span data-ttu-id="72323-104">句法</span><span class="sxs-lookup"><span data-stu-id="72323-104">SYNTAX</span></span>

### <span data-ttu-id="72323-105">ByAll (預設) </span><span class="sxs-lookup"><span data-stu-id="72323-105">ByAll (Default)</span></span>
```
Get-AzureAutomationModule -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="72323-106">ByName</span><span class="sxs-lookup"><span data-stu-id="72323-106">ByName</span></span>
```
Get-AzureAutomationModule -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="72323-107">說明</span><span class="sxs-lookup"><span data-stu-id="72323-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="72323-108">**AzureAutomationModule** Cmdlet 會取得一或多個 Microsoft Azure 自動化模組。</span><span class="sxs-lookup"><span data-stu-id="72323-108">The **Get-AzureAutomationModule** cmdlet gets one or more Microsoft Azure Automation modules.</span></span>
<span data-ttu-id="72323-109">根據預設，會傳回所有的模組。</span><span class="sxs-lookup"><span data-stu-id="72323-109">By default, all modules are returned.</span></span>
<span data-ttu-id="72323-110">若要取得特定的模組，請指定其名稱。</span><span class="sxs-lookup"><span data-stu-id="72323-110">To get a specific module, specify its name.</span></span>

## <span data-ttu-id="72323-111">示例</span><span class="sxs-lookup"><span data-stu-id="72323-111">EXAMPLES</span></span>

### <span data-ttu-id="72323-112">範例1：取得所有模組</span><span class="sxs-lookup"><span data-stu-id="72323-112">Example 1: Get all modules</span></span>
```
PS C:\> Get-AzureAutomationModule -AutomationAccountName "Contoso17"
```

<span data-ttu-id="72323-113">這個命令會取得 Azure 自動化帳戶（名為 Contoso17）中的所有模組。</span><span class="sxs-lookup"><span data-stu-id="72323-113">This command gets all modules in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="72323-114">範例2：取得模組</span><span class="sxs-lookup"><span data-stu-id="72323-114">Example 2: Get a module</span></span>
```
PS C:\> Get-AzureAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule"
```

<span data-ttu-id="72323-115">這個命令會在 Azure 自動化帳戶（名為 Contoso17）中取得名為 ContosoModule 的模組。</span><span class="sxs-lookup"><span data-stu-id="72323-115">This command gets a module named ContosoModule in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="72323-116">參數</span><span class="sxs-lookup"><span data-stu-id="72323-116">PARAMETERS</span></span>

### <span data-ttu-id="72323-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="72323-117">-AutomationAccountName</span></span>
<span data-ttu-id="72323-118">指定要取得 runbook 的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="72323-118">Specifies the name of the Automation account with the runbook to retrieve.</span></span>

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

### <span data-ttu-id="72323-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="72323-119">-Name</span></span>
<span data-ttu-id="72323-120">指定要檢索的模組名稱。</span><span class="sxs-lookup"><span data-stu-id="72323-120">Specifies the name of a module to retrieve.</span></span>

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

### <span data-ttu-id="72323-121">-設定檔</span><span class="sxs-lookup"><span data-stu-id="72323-121">-Profile</span></span>
<span data-ttu-id="72323-122">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="72323-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="72323-123">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="72323-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="72323-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72323-124">CommonParameters</span></span>
<span data-ttu-id="72323-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="72323-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72323-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="72323-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72323-127">輸入</span><span class="sxs-lookup"><span data-stu-id="72323-127">INPUTS</span></span>

## <span data-ttu-id="72323-128">輸出</span><span class="sxs-lookup"><span data-stu-id="72323-128">OUTPUTS</span></span>

### <span data-ttu-id="72323-129">[-Azure. 命令. Model. Module]</span><span class="sxs-lookup"><span data-stu-id="72323-129">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="72323-130">筆記</span><span class="sxs-lookup"><span data-stu-id="72323-130">NOTES</span></span>

## <span data-ttu-id="72323-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="72323-131">RELATED LINKS</span></span>

[<span data-ttu-id="72323-132">新-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="72323-132">New-AzureAutomationModule</span></span>](./New-AzureAutomationModule.md)

[<span data-ttu-id="72323-133">移除-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="72323-133">Remove-AzureAutomationModule</span></span>](./Remove-AzureAutomationModule.md)

[<span data-ttu-id="72323-134">Set-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="72323-134">Set-AzureAutomationModule</span></span>](./Set-AzureAutomationModule.md)


