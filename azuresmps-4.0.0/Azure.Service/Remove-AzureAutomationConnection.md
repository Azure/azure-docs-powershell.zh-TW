---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: DDEBA3E1-B5A3-4F16-9A67-A95D15851A33
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0899349c3dbfa368b3ce0dbb4d4085c3ea527c43
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967938"
---
# <span data-ttu-id="b0ac3-101">Remove-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="b0ac3-101">Remove-AzureAutomationConnection</span></span>

## <span data-ttu-id="b0ac3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b0ac3-102">SYNOPSIS</span></span>

<span data-ttu-id="b0ac3-103">從 [自動化] 移除連線。</span><span class="sxs-lookup"><span data-stu-id="b0ac3-103">Removes a connection from Automation.</span></span>

## <span data-ttu-id="b0ac3-104">句法</span><span class="sxs-lookup"><span data-stu-id="b0ac3-104">SYNTAX</span></span>

```
Remove-AzureAutomationConnection -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b0ac3-105">說明</span><span class="sxs-lookup"><span data-stu-id="b0ac3-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="b0ac3-106">**AzureAutomationConnection** Cmdlet 會從 Microsoft Azure 自動化中移除連線。</span><span class="sxs-lookup"><span data-stu-id="b0ac3-106">The **Remove-AzureAutomationConnection** cmdlet removes a connection from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="b0ac3-107">示例</span><span class="sxs-lookup"><span data-stu-id="b0ac3-107">EXAMPLES</span></span>

### <span data-ttu-id="b0ac3-108">範例1：移除連線</span><span class="sxs-lookup"><span data-stu-id="b0ac3-108">Example 1: Remove a connection</span></span>
```
PS C:\> Remove-AzureAutomationConnection -AutomationAccountName "Contoso17" -Name "MyConnection"
```

<span data-ttu-id="b0ac3-109">這個命令會在名為 [Contoso17] 的自動化帳戶中移除名為連線的憑證。</span><span class="sxs-lookup"><span data-stu-id="b0ac3-109">This command removes a certificate named MyConnection in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="b0ac3-110">參數</span><span class="sxs-lookup"><span data-stu-id="b0ac3-110">PARAMETERS</span></span>

### <span data-ttu-id="b0ac3-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b0ac3-111">-AutomationAccountName</span></span>
<span data-ttu-id="b0ac3-112">指定含認證之自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="b0ac3-112">Specifies the name of the Automation account with the credential.</span></span>

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

### <span data-ttu-id="b0ac3-113">-Force</span><span class="sxs-lookup"><span data-stu-id="b0ac3-113">-Force</span></span>
<span data-ttu-id="b0ac3-114">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="b0ac3-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b0ac3-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="b0ac3-115">-Name</span></span>
<span data-ttu-id="b0ac3-116">指定連線的名稱。</span><span class="sxs-lookup"><span data-stu-id="b0ac3-116">Specifies the name of the connection.</span></span>

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

### <span data-ttu-id="b0ac3-117">-設定檔</span><span class="sxs-lookup"><span data-stu-id="b0ac3-117">-Profile</span></span>
<span data-ttu-id="b0ac3-118">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="b0ac3-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b0ac3-119">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="b0ac3-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b0ac3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0ac3-120">CommonParameters</span></span>
<span data-ttu-id="b0ac3-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b0ac3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0ac3-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b0ac3-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0ac3-123">輸入</span><span class="sxs-lookup"><span data-stu-id="b0ac3-123">INPUTS</span></span>

## <span data-ttu-id="b0ac3-124">輸出</span><span class="sxs-lookup"><span data-stu-id="b0ac3-124">OUTPUTS</span></span>

## <span data-ttu-id="b0ac3-125">筆記</span><span class="sxs-lookup"><span data-stu-id="b0ac3-125">NOTES</span></span>

## <span data-ttu-id="b0ac3-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="b0ac3-126">RELATED LINKS</span></span>

[<span data-ttu-id="b0ac3-127">AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="b0ac3-127">Get-AzureAutomationConnection</span></span>](./Get-AzureAutomationConnection.md)

[<span data-ttu-id="b0ac3-128">新-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="b0ac3-128">New-AzureAutomationConnection</span></span>](./New-AzureAutomationConnection.md)

[<span data-ttu-id="b0ac3-129">Set-AzureAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="b0ac3-129">Set-AzureAutomationConnectionFieldValue</span></span>](./Set-AzureAutomationConnectionFieldValue.md)


