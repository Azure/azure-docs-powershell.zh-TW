---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 4D87DD30-4AEF-4269-93B2-AE5964334AC8
online version: ''
schema: 2.0.0
ms.openlocfilehash: b581712f020b8168c052634e0f20244e16a7d950
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967926"
---
# <span data-ttu-id="dc1da-101">Remove-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="dc1da-101">Remove-AzureAutomationCredential</span></span>

## <span data-ttu-id="dc1da-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dc1da-102">SYNOPSIS</span></span>

<span data-ttu-id="dc1da-103">從 [自動化] 移除認證。</span><span class="sxs-lookup"><span data-stu-id="dc1da-103">Removes a credential from Automation.</span></span>

## <span data-ttu-id="dc1da-104">句法</span><span class="sxs-lookup"><span data-stu-id="dc1da-104">SYNTAX</span></span>

```
Remove-AzureAutomationCredential -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="dc1da-105">說明</span><span class="sxs-lookup"><span data-stu-id="dc1da-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="dc1da-106">**AzureAutomationCredential** Cmdlet 會從 Microsoft Azure 自動化中移除認證。</span><span class="sxs-lookup"><span data-stu-id="dc1da-106">The **Remove-AzureAutomationCredential** cmdlet removes a credential from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="dc1da-107">示例</span><span class="sxs-lookup"><span data-stu-id="dc1da-107">EXAMPLES</span></span>

### <span data-ttu-id="dc1da-108">範例1：移除認證</span><span class="sxs-lookup"><span data-stu-id="dc1da-108">Example 1: Remove a credential</span></span>
```
PS C:\> Remove-AzureAutomationCredential -AutomationAccountName "Contoso17" -Name "MyCredential"
```

<span data-ttu-id="dc1da-109">這個命令會在名為 [Contoso17] 的自動化帳戶中移除一個名為 MyCredential 的認證。</span><span class="sxs-lookup"><span data-stu-id="dc1da-109">This command removes a credential named MyCredential in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="dc1da-110">參數</span><span class="sxs-lookup"><span data-stu-id="dc1da-110">PARAMETERS</span></span>

### <span data-ttu-id="dc1da-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="dc1da-111">-AutomationAccountName</span></span>
<span data-ttu-id="dc1da-112">指定含認證之自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="dc1da-112">Specifies the name of the Automation account with the credential.</span></span>

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

### <span data-ttu-id="dc1da-113">-Force</span><span class="sxs-lookup"><span data-stu-id="dc1da-113">-Force</span></span>
<span data-ttu-id="dc1da-114">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="dc1da-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="dc1da-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="dc1da-115">-Name</span></span>
<span data-ttu-id="dc1da-116">指定要移除之認證的名稱。</span><span class="sxs-lookup"><span data-stu-id="dc1da-116">Specifies the name of the credential to remove.</span></span>

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

### <span data-ttu-id="dc1da-117">-設定檔</span><span class="sxs-lookup"><span data-stu-id="dc1da-117">-Profile</span></span>
<span data-ttu-id="dc1da-118">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="dc1da-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="dc1da-119">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="dc1da-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="dc1da-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc1da-120">CommonParameters</span></span>
<span data-ttu-id="dc1da-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dc1da-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc1da-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="dc1da-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc1da-123">輸入</span><span class="sxs-lookup"><span data-stu-id="dc1da-123">INPUTS</span></span>

## <span data-ttu-id="dc1da-124">輸出</span><span class="sxs-lookup"><span data-stu-id="dc1da-124">OUTPUTS</span></span>

## <span data-ttu-id="dc1da-125">筆記</span><span class="sxs-lookup"><span data-stu-id="dc1da-125">NOTES</span></span>

## <span data-ttu-id="dc1da-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="dc1da-126">RELATED LINKS</span></span>

[<span data-ttu-id="dc1da-127">AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="dc1da-127">Get-AzureAutomationCredential</span></span>](./Get-AzureAutomationCredential.md)

[<span data-ttu-id="dc1da-128">新-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="dc1da-128">New-AzureAutomationCredential</span></span>](./New-AzureAutomationCredential.md)

[<span data-ttu-id="dc1da-129">Set-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="dc1da-129">Set-AzureAutomationCredential</span></span>](./Set-AzureAutomationCredential.md)


