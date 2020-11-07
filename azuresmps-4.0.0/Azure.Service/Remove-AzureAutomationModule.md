---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 73BE191D-816F-4376-8304-B0ABA4163EF6
online version: ''
schema: 2.0.0
ms.openlocfilehash: a75016368a770221fd0ab373a4b59c5975ee2a24
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967927"
---
# <span data-ttu-id="836b8-101">Remove-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="836b8-101">Remove-AzureAutomationModule</span></span>

## <span data-ttu-id="836b8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="836b8-102">SYNOPSIS</span></span>

<span data-ttu-id="836b8-103">從自動化中移除模組。</span><span class="sxs-lookup"><span data-stu-id="836b8-103">Removes a module from Automation.</span></span>

## <span data-ttu-id="836b8-104">句法</span><span class="sxs-lookup"><span data-stu-id="836b8-104">SYNTAX</span></span>

```
Remove-AzureAutomationModule -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="836b8-105">說明</span><span class="sxs-lookup"><span data-stu-id="836b8-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="836b8-106">**AzureAutomationModule** Cmdlet 會從 Microsoft Azure 自動化中移除自動化帳戶。</span><span class="sxs-lookup"><span data-stu-id="836b8-106">The **Remove-AzureAutomationModule** cmdlet removes an Automation account from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="836b8-107">示例</span><span class="sxs-lookup"><span data-stu-id="836b8-107">EXAMPLES</span></span>

### <span data-ttu-id="836b8-108">範例1：移除模組</span><span class="sxs-lookup"><span data-stu-id="836b8-108">Example 1: Remove a module</span></span>
```
PS C:\> Remove-AzureAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule"
```

<span data-ttu-id="836b8-109">這個命令會從名為 Contoso17 的自動化帳戶中移除名為 ContosoModule 的模組。</span><span class="sxs-lookup"><span data-stu-id="836b8-109">This command removes a module named ContosoModule from the Automation account named Contoso17.</span></span>

## <span data-ttu-id="836b8-110">參數</span><span class="sxs-lookup"><span data-stu-id="836b8-110">PARAMETERS</span></span>

### <span data-ttu-id="836b8-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="836b8-111">-AutomationAccountName</span></span>
<span data-ttu-id="836b8-112">指定模組的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="836b8-112">Specifies the name of the Automation account with the module.</span></span>

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

### <span data-ttu-id="836b8-113">-Force</span><span class="sxs-lookup"><span data-stu-id="836b8-113">-Force</span></span>
<span data-ttu-id="836b8-114">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="836b8-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="836b8-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="836b8-115">-Name</span></span>
<span data-ttu-id="836b8-116">指定要移除的模組名稱。</span><span class="sxs-lookup"><span data-stu-id="836b8-116">Specifies the name of the module to remove.</span></span>

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

### <span data-ttu-id="836b8-117">-設定檔</span><span class="sxs-lookup"><span data-stu-id="836b8-117">-Profile</span></span>
<span data-ttu-id="836b8-118">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="836b8-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="836b8-119">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="836b8-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="836b8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="836b8-120">CommonParameters</span></span>
<span data-ttu-id="836b8-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="836b8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="836b8-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="836b8-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="836b8-123">輸入</span><span class="sxs-lookup"><span data-stu-id="836b8-123">INPUTS</span></span>

## <span data-ttu-id="836b8-124">輸出</span><span class="sxs-lookup"><span data-stu-id="836b8-124">OUTPUTS</span></span>

## <span data-ttu-id="836b8-125">筆記</span><span class="sxs-lookup"><span data-stu-id="836b8-125">NOTES</span></span>

## <span data-ttu-id="836b8-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="836b8-126">RELATED LINKS</span></span>

[<span data-ttu-id="836b8-127">AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="836b8-127">Get-AzureAutomationModule</span></span>](./Get-AzureAutomationModule.md)

[<span data-ttu-id="836b8-128">新-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="836b8-128">New-AzureAutomationModule</span></span>](./New-AzureAutomationModule.md)

[<span data-ttu-id="836b8-129">Set-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="836b8-129">Set-AzureAutomationModule</span></span>](./Set-AzureAutomationModule.md)


