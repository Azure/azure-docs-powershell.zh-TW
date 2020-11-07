---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 2D89557B-4B8B-43EE-8453-D55FCE0C2CE0
online version: ''
schema: 2.0.0
ms.openlocfilehash: f8fdd9dd886e4056f2cb7e547098e5d3ab75a547
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967615"
---
# <span data-ttu-id="42627-101">Remove-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="42627-101">Remove-AzureAutomationVariable</span></span>

## <span data-ttu-id="42627-102">摘要</span><span class="sxs-lookup"><span data-stu-id="42627-102">SYNOPSIS</span></span>

<span data-ttu-id="42627-103">移除自動化變數。</span><span class="sxs-lookup"><span data-stu-id="42627-103">Removes an Automation variable.</span></span>

## <span data-ttu-id="42627-104">句法</span><span class="sxs-lookup"><span data-stu-id="42627-104">SYNTAX</span></span>

```
Remove-AzureAutomationVariable -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="42627-105">說明</span><span class="sxs-lookup"><span data-stu-id="42627-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="42627-106">**AzureAutomationVariable** Cmdlet 會從 Microsoft Azure 自動化中移除變數。</span><span class="sxs-lookup"><span data-stu-id="42627-106">The **Remove-AzureAutomationVariable** cmdlet removes a variable from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="42627-107">示例</span><span class="sxs-lookup"><span data-stu-id="42627-107">EXAMPLES</span></span>

### <span data-ttu-id="42627-108">範例1：移除變數</span><span class="sxs-lookup"><span data-stu-id="42627-108">Example 1: Remove a variable</span></span>
```
PS C:\> Remove-AzureAutomationVariable -AutomationAccountName "Contoso17" -Name "MyStringVariable" -Force
```

<span data-ttu-id="42627-109">這個命令會在自動帳戶（名為 Contoso17）中移除名為 MyStringVariable 的變數，但不會提示使用者驗證。</span><span class="sxs-lookup"><span data-stu-id="42627-109">This command removes a variable named MyStringVariable in the Automation account named Contoso17 without prompting for user validation.</span></span>

## <span data-ttu-id="42627-110">參數</span><span class="sxs-lookup"><span data-stu-id="42627-110">PARAMETERS</span></span>

### <span data-ttu-id="42627-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="42627-111">-AutomationAccountName</span></span>
<span data-ttu-id="42627-112">使用變數指定自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="42627-112">Specifies the name of the Automation account with the variable.</span></span>

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

### <span data-ttu-id="42627-113">-Force</span><span class="sxs-lookup"><span data-stu-id="42627-113">-Force</span></span>
<span data-ttu-id="42627-114">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="42627-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42627-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="42627-115">-Name</span></span>
<span data-ttu-id="42627-116">指定變數的名稱。</span><span class="sxs-lookup"><span data-stu-id="42627-116">Specifies the name of the variable.</span></span>

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

### <span data-ttu-id="42627-117">-設定檔</span><span class="sxs-lookup"><span data-stu-id="42627-117">-Profile</span></span>
<span data-ttu-id="42627-118">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="42627-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="42627-119">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="42627-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="42627-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42627-120">CommonParameters</span></span>
<span data-ttu-id="42627-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="42627-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42627-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="42627-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42627-123">輸入</span><span class="sxs-lookup"><span data-stu-id="42627-123">INPUTS</span></span>

## <span data-ttu-id="42627-124">輸出</span><span class="sxs-lookup"><span data-stu-id="42627-124">OUTPUTS</span></span>

## <span data-ttu-id="42627-125">筆記</span><span class="sxs-lookup"><span data-stu-id="42627-125">NOTES</span></span>

## <span data-ttu-id="42627-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="42627-126">RELATED LINKS</span></span>

[<span data-ttu-id="42627-127">AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="42627-127">Get-AzureAutomationVariable</span></span>](./Get-AzureAutomationVariable.md)

[<span data-ttu-id="42627-128">新-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="42627-128">New-AzureAutomationVariable</span></span>](./New-AzureAutomationVariable.md)

[<span data-ttu-id="42627-129">Set-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="42627-129">Set-AzureAutomationVariable</span></span>](./Set-AzureAutomationVariable.md)


