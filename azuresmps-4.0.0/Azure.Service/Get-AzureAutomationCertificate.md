---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: FED10AA9-DD3A-4034-B78E-F9E55290B353
online version: ''
schema: 2.0.0
ms.openlocfilehash: 272969751988d3747788c2a214e8eb7ed509f232
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967109"
---
# <span data-ttu-id="ede46-101">Get-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="ede46-101">Get-AzureAutomationCertificate</span></span>

## <span data-ttu-id="ede46-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ede46-102">SYNOPSIS</span></span>

<span data-ttu-id="ede46-103">取得 Azure 自動化憑證。</span><span class="sxs-lookup"><span data-stu-id="ede46-103">Gets an Azure Automation certificate.</span></span>

## <span data-ttu-id="ede46-104">句法</span><span class="sxs-lookup"><span data-stu-id="ede46-104">SYNTAX</span></span>

### <span data-ttu-id="ede46-105">ByAll (預設) </span><span class="sxs-lookup"><span data-stu-id="ede46-105">ByAll (Default)</span></span>
```
Get-AzureAutomationCertificate -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="ede46-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="ede46-106">ByCertificateName</span></span>
```
Get-AzureAutomationCertificate -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="ede46-107">說明</span><span class="sxs-lookup"><span data-stu-id="ede46-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="ede46-108">**AzureAutomationCertificate** Cmdlet 會取得一或多個 Microsoft Azure 自動化憑證。</span><span class="sxs-lookup"><span data-stu-id="ede46-108">The **Get-AzureAutomationCertificate** cmdlet gets one or more Microsoft Azure Automation certificates.</span></span>
<span data-ttu-id="ede46-109">根據預設，會傳回所有憑證。</span><span class="sxs-lookup"><span data-stu-id="ede46-109">By default, all certificates are returned.</span></span>
<span data-ttu-id="ede46-110">若要取得特定憑證，請指定其名稱。</span><span class="sxs-lookup"><span data-stu-id="ede46-110">To get a specific certificate, specify its name.</span></span>

## <span data-ttu-id="ede46-111">示例</span><span class="sxs-lookup"><span data-stu-id="ede46-111">EXAMPLES</span></span>

### <span data-ttu-id="ede46-112">範例1：取得所有憑證</span><span class="sxs-lookup"><span data-stu-id="ede46-112">Example 1: Get all certificates</span></span>
```
PS C:\> Get-AzureAutomationCertificate -AutomationAccountName "Contoso17"
```

<span data-ttu-id="ede46-113">這個命令會取得 Azure 自動化帳戶（名為 Contoso17）中的所有憑證。</span><span class="sxs-lookup"><span data-stu-id="ede46-113">This command gets all certificates in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="ede46-114">範例2：取得憑證</span><span class="sxs-lookup"><span data-stu-id="ede46-114">Example 2: Get a certificate</span></span>
```
PS C:\> Get-AzureAutomationCertificate -AutomationAccountName "Contoso17" -Name "MyUserCertificate"
```

<span data-ttu-id="ede46-115">這個命令會取得名為 MyUserCertificate 的憑證。</span><span class="sxs-lookup"><span data-stu-id="ede46-115">This command gets the certificate named MyUserCertificate.</span></span>

## <span data-ttu-id="ede46-116">參數</span><span class="sxs-lookup"><span data-stu-id="ede46-116">PARAMETERS</span></span>

### <span data-ttu-id="ede46-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ede46-117">-AutomationAccountName</span></span>
<span data-ttu-id="ede46-118">指定憑證的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="ede46-118">Specifies the name of the automation account with the certificate.</span></span>

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

### <span data-ttu-id="ede46-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="ede46-119">-Name</span></span>
<span data-ttu-id="ede46-120">指定要檢索之憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="ede46-120">Specifies the name of a certificate to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: ByCertificateName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ede46-121">-設定檔</span><span class="sxs-lookup"><span data-stu-id="ede46-121">-Profile</span></span>
<span data-ttu-id="ede46-122">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="ede46-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ede46-123">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="ede46-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ede46-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ede46-124">CommonParameters</span></span>
<span data-ttu-id="ede46-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ede46-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ede46-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ede46-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ede46-127">輸入</span><span class="sxs-lookup"><span data-stu-id="ede46-127">INPUTS</span></span>

## <span data-ttu-id="ede46-128">輸出</span><span class="sxs-lookup"><span data-stu-id="ede46-128">OUTPUTS</span></span>

### <span data-ttu-id="ede46-129">CertificateInfo 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ede46-129">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="ede46-130">筆記</span><span class="sxs-lookup"><span data-stu-id="ede46-130">NOTES</span></span>

## <span data-ttu-id="ede46-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="ede46-131">RELATED LINKS</span></span>

[<span data-ttu-id="ede46-132">新-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="ede46-132">New-AzureAutomationCertificate</span></span>](./New-AzureAutomationCertificate.md)

[<span data-ttu-id="ede46-133">移除-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="ede46-133">Remove-AzureAutomationCertificate</span></span>](./Remove-AzureAutomationCertificate.md)

[<span data-ttu-id="ede46-134">Set-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="ede46-134">Set-AzureAutomationCertificate</span></span>](./Set-AzureAutomationCertificate.md)


