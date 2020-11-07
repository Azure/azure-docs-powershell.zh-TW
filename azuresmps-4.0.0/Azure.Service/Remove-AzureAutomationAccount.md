---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: B8E4F6BD-FBF2-4B19-AA61-02149F933ABB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 52cba1ea3d42640693f2f330bf158a1eb078eebc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967941"
---
# <span data-ttu-id="35988-101">Remove-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="35988-101">Remove-AzureAutomationAccount</span></span>

## <span data-ttu-id="35988-102">摘要</span><span class="sxs-lookup"><span data-stu-id="35988-102">SYNOPSIS</span></span>

<span data-ttu-id="35988-103">移除自動化帳戶。</span><span class="sxs-lookup"><span data-stu-id="35988-103">Removes an Automation Account.</span></span>

## <span data-ttu-id="35988-104">句法</span><span class="sxs-lookup"><span data-stu-id="35988-104">SYNTAX</span></span>

```
Remove-AzureAutomationAccount -Name <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="35988-105">說明</span><span class="sxs-lookup"><span data-stu-id="35988-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="35988-106">**AzureAutomationAccount** Cmdlet 會從 Microsoft Azure 自動化中移除帳戶。</span><span class="sxs-lookup"><span data-stu-id="35988-106">The **Remove-AzureAutomationAccount** cmdlet removes an account from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="35988-107">示例</span><span class="sxs-lookup"><span data-stu-id="35988-107">EXAMPLES</span></span>

### <span data-ttu-id="35988-108">範例1：移除自動化帳戶</span><span class="sxs-lookup"><span data-stu-id="35988-108">Example 1: Remove an Automation account</span></span>
```
PS C:\> Remove-AzureAutomationAccount -Name "MyAutomationAccount" -Force
```

<span data-ttu-id="35988-109">這個命令會移除一個名為 MyAutomationAccount 的自動化帳戶，但不會提示使用者驗證。</span><span class="sxs-lookup"><span data-stu-id="35988-109">This command removes an Automation account named MyAutomationAccount without prompting for user validation.</span></span>

## <span data-ttu-id="35988-110">參數</span><span class="sxs-lookup"><span data-stu-id="35988-110">PARAMETERS</span></span>

### <span data-ttu-id="35988-111">-Force</span><span class="sxs-lookup"><span data-stu-id="35988-111">-Force</span></span>
<span data-ttu-id="35988-112">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="35988-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="35988-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="35988-113">-Name</span></span>
<span data-ttu-id="35988-114">指定自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="35988-114">Specifies the name of the Automation account.</span></span>

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

### <span data-ttu-id="35988-115">-設定檔</span><span class="sxs-lookup"><span data-stu-id="35988-115">-Profile</span></span>
<span data-ttu-id="35988-116">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="35988-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="35988-117">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="35988-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="35988-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35988-118">CommonParameters</span></span>
<span data-ttu-id="35988-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="35988-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35988-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="35988-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35988-121">輸入</span><span class="sxs-lookup"><span data-stu-id="35988-121">INPUTS</span></span>

## <span data-ttu-id="35988-122">輸出</span><span class="sxs-lookup"><span data-stu-id="35988-122">OUTPUTS</span></span>

## <span data-ttu-id="35988-123">筆記</span><span class="sxs-lookup"><span data-stu-id="35988-123">NOTES</span></span>

## <span data-ttu-id="35988-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="35988-124">RELATED LINKS</span></span>

[<span data-ttu-id="35988-125">AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="35988-125">Get-AzureAutomationAccount</span></span>](./Get-AzureAutomationAccount.md)

[<span data-ttu-id="35988-126">新-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="35988-126">New-AzureAutomationAccount</span></span>](./New-AzureAutomationAccount.md)


