---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 59CDE74B-EFB3-4904-A482-466B0EA17F4B
online version: ''
schema: 2.0.0
ms.openlocfilehash: a787193669cab32a43b7c9b9eb2010a6e545539b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967670"
---
# <span data-ttu-id="e4fb7-101">New-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="e4fb7-101">New-AzureAutomationAccount</span></span>

## <span data-ttu-id="e4fb7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e4fb7-102">SYNOPSIS</span></span>

<span data-ttu-id="e4fb7-103">建立自動化帳戶。</span><span class="sxs-lookup"><span data-stu-id="e4fb7-103">Creates an Automation account.</span></span>

## <span data-ttu-id="e4fb7-104">句法</span><span class="sxs-lookup"><span data-stu-id="e4fb7-104">SYNTAX</span></span>

```
New-AzureAutomationAccount -Name <String> -Location <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e4fb7-105">說明</span><span class="sxs-lookup"><span data-stu-id="e4fb7-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="e4fb7-106">**新的-AzureAutomationAccount** Cmdlet 會在 Microsoft Azure 自動化中建立新帳戶。</span><span class="sxs-lookup"><span data-stu-id="e4fb7-106">The **New-AzureAutomationAccount** cmdlet creates a new account in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="e4fb7-107">示例</span><span class="sxs-lookup"><span data-stu-id="e4fb7-107">EXAMPLES</span></span>

### <span data-ttu-id="e4fb7-108">範例1：建立自動化帳戶</span><span class="sxs-lookup"><span data-stu-id="e4fb7-108">Example 1: Create an Automation account</span></span>
```
PS C:\> New-AzureAutomationAccount -Name "MyAutomationAccount" -Location "East US"
```

<span data-ttu-id="e4fb7-109">這個命令會在東美國地區建立名為 MyAutomationAccount 的自動化帳戶。</span><span class="sxs-lookup"><span data-stu-id="e4fb7-109">This command creates an Automation account named MyAutomationAccount in the East US region.</span></span>

## <span data-ttu-id="e4fb7-110">參數</span><span class="sxs-lookup"><span data-stu-id="e4fb7-110">PARAMETERS</span></span>

### <span data-ttu-id="e4fb7-111">-位置</span><span class="sxs-lookup"><span data-stu-id="e4fb7-111">-Location</span></span>
<span data-ttu-id="e4fb7-112">指定帳戶的位置。</span><span class="sxs-lookup"><span data-stu-id="e4fb7-112">Specifies the location of the account.</span></span>

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

### <span data-ttu-id="e4fb7-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="e4fb7-113">-Name</span></span>
<span data-ttu-id="e4fb7-114">指定帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="e4fb7-114">Specifies the name of the account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4fb7-115">-設定檔</span><span class="sxs-lookup"><span data-stu-id="e4fb7-115">-Profile</span></span>
<span data-ttu-id="e4fb7-116">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="e4fb7-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e4fb7-117">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="e4fb7-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e4fb7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4fb7-118">CommonParameters</span></span>
<span data-ttu-id="e4fb7-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e4fb7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4fb7-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e4fb7-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4fb7-121">輸入</span><span class="sxs-lookup"><span data-stu-id="e4fb7-121">INPUTS</span></span>

## <span data-ttu-id="e4fb7-122">輸出</span><span class="sxs-lookup"><span data-stu-id="e4fb7-122">OUTPUTS</span></span>

### <span data-ttu-id="e4fb7-123">AutomationAccount 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e4fb7-123">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="e4fb7-124">筆記</span><span class="sxs-lookup"><span data-stu-id="e4fb7-124">NOTES</span></span>

## <span data-ttu-id="e4fb7-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="e4fb7-125">RELATED LINKS</span></span>

[<span data-ttu-id="e4fb7-126">AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="e4fb7-126">Get-AzureAutomationAccount</span></span>](./Get-AzureAutomationAccount.md)

[<span data-ttu-id="e4fb7-127">移除-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="e4fb7-127">Remove-AzureAutomationAccount</span></span>](./Remove-AzureAutomationAccount.md)


