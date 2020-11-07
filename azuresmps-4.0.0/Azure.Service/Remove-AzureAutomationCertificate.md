---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: BCF8DAB4-3E14-463B-A18F-E91C740B0D3A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 08dd82489bf02efa167386300b9b1d565e1a63de
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967939"
---
# <span data-ttu-id="3e104-101">Remove-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="3e104-101">Remove-AzureAutomationCertificate</span></span>

## <span data-ttu-id="3e104-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3e104-102">SYNOPSIS</span></span>

<span data-ttu-id="3e104-103">移除自動化憑證。</span><span class="sxs-lookup"><span data-stu-id="3e104-103">Removes an Automation certificate.</span></span>

## <span data-ttu-id="3e104-104">句法</span><span class="sxs-lookup"><span data-stu-id="3e104-104">SYNTAX</span></span>

```
Remove-AzureAutomationCertificate -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3e104-105">說明</span><span class="sxs-lookup"><span data-stu-id="3e104-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="3e104-106">**AzureAutomationAccount** Cmdlet 會從 Microsoft Azure 自動化中移除證書。</span><span class="sxs-lookup"><span data-stu-id="3e104-106">The **Remove-AzureAutomationAccount** cmdlet removes a certificate from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="3e104-107">示例</span><span class="sxs-lookup"><span data-stu-id="3e104-107">EXAMPLES</span></span>

### <span data-ttu-id="3e104-108">範例1：移除憑證</span><span class="sxs-lookup"><span data-stu-id="3e104-108">Example 1: Remove a certificate</span></span>
```
PS C:\> Remove-AzureAutomationCertificate -AutomationAccountName "Contoso17" -Name "Cert01"
```

<span data-ttu-id="3e104-109">這個命令會在名為 [Contoso17] 的自動化帳戶中移除名為 Cert01 的憑證。</span><span class="sxs-lookup"><span data-stu-id="3e104-109">This command removes a certificate named Cert01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="3e104-110">參數</span><span class="sxs-lookup"><span data-stu-id="3e104-110">PARAMETERS</span></span>

### <span data-ttu-id="3e104-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3e104-111">-AutomationAccountName</span></span>
<span data-ttu-id="3e104-112">指定憑證的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="3e104-112">Specifies the name of the Automation account with the certificate.</span></span>

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

### <span data-ttu-id="3e104-113">-Force</span><span class="sxs-lookup"><span data-stu-id="3e104-113">-Force</span></span>
<span data-ttu-id="3e104-114">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="3e104-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3e104-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="3e104-115">-Name</span></span>
<span data-ttu-id="3e104-116">指定憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="3e104-116">Specifies the name of the certificate.</span></span>

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

### <span data-ttu-id="3e104-117">-設定檔</span><span class="sxs-lookup"><span data-stu-id="3e104-117">-Profile</span></span>
<span data-ttu-id="3e104-118">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="3e104-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3e104-119">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="3e104-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3e104-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e104-120">CommonParameters</span></span>
<span data-ttu-id="3e104-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3e104-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e104-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3e104-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e104-123">輸入</span><span class="sxs-lookup"><span data-stu-id="3e104-123">INPUTS</span></span>

## <span data-ttu-id="3e104-124">輸出</span><span class="sxs-lookup"><span data-stu-id="3e104-124">OUTPUTS</span></span>

## <span data-ttu-id="3e104-125">筆記</span><span class="sxs-lookup"><span data-stu-id="3e104-125">NOTES</span></span>

## <span data-ttu-id="3e104-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="3e104-126">RELATED LINKS</span></span>

[<span data-ttu-id="3e104-127">AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="3e104-127">Get-AzureAutomationCertificate</span></span>](./Get-AzureAutomationCertificate.md)

[<span data-ttu-id="3e104-128">新-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="3e104-128">New-AzureAutomationCertificate</span></span>](./New-AzureAutomationCertificate.md)

[<span data-ttu-id="3e104-129">Set-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="3e104-129">Set-AzureAutomationCertificate</span></span>](./Set-AzureAutomationCertificate.md)


