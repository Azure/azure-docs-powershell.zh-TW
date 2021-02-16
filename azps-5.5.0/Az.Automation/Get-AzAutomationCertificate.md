---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D690C903-A481-45F2-9D42-1CE2F4184A98
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCertificate.md
ms.openlocfilehash: 3a504ba081852ff3bb84a6ace432b394a2b2b478
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100139630"
---
# <span data-ttu-id="1d975-101">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="1d975-101">Get-AzAutomationCertificate</span></span>

## <span data-ttu-id="1d975-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1d975-102">SYNOPSIS</span></span>
<span data-ttu-id="1d975-103">取得自動化憑證。</span><span class="sxs-lookup"><span data-stu-id="1d975-103">Gets Automation certificates.</span></span>

## <span data-ttu-id="1d975-104">句法</span><span class="sxs-lookup"><span data-stu-id="1d975-104">SYNTAX</span></span>

### <span data-ttu-id="1d975-105">ByAll (預設) </span><span class="sxs-lookup"><span data-stu-id="1d975-105">ByAll (Default)</span></span>
```
Get-AzAutomationCertificate [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d975-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="1d975-106">ByCertificateName</span></span>
```
Get-AzAutomationCertificate [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d975-107">說明</span><span class="sxs-lookup"><span data-stu-id="1d975-107">DESCRIPTION</span></span>
<span data-ttu-id="1d975-108">**AzAutomationCertificate** Cmdlet 會取得一或多個 Azure 自動化憑證。</span><span class="sxs-lookup"><span data-stu-id="1d975-108">The **Get-AzAutomationCertificate** cmdlet gets one or more Azure Automation certificates.</span></span>
<span data-ttu-id="1d975-109">根據預設，這個 Cmdlet 會取得所有憑證。</span><span class="sxs-lookup"><span data-stu-id="1d975-109">By default, this cmdlet gets all certificates.</span></span>
<span data-ttu-id="1d975-110">指定要取得特定憑證的憑證名稱。</span><span class="sxs-lookup"><span data-stu-id="1d975-110">Specify the name of a certificate to get a specific certificate.</span></span>

## <span data-ttu-id="1d975-111">示例</span><span class="sxs-lookup"><span data-stu-id="1d975-111">EXAMPLES</span></span>

### <span data-ttu-id="1d975-112">範例1：取得所有憑證</span><span class="sxs-lookup"><span data-stu-id="1d975-112">Example 1: Get all certificates</span></span>
```
PS C:\>Get-AzAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="1d975-113">這個命令會針對自動化帳戶中名為 Contoso17 的所有憑證取得中繼資料。</span><span class="sxs-lookup"><span data-stu-id="1d975-113">This command gets metadata for all certificates in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="1d975-114">範例2：取得憑證</span><span class="sxs-lookup"><span data-stu-id="1d975-114">Example 2: Get a certificate</span></span>
```
PS C:\>Get-AzAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17" -Name "ContosoCertificate"
```

<span data-ttu-id="1d975-115">這個命令會取得名為 ContosoCertificate 的憑證的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="1d975-115">This command gets metadata for the certificate named ContosoCertificate.</span></span>

## <span data-ttu-id="1d975-116">參數</span><span class="sxs-lookup"><span data-stu-id="1d975-116">PARAMETERS</span></span>

### <span data-ttu-id="1d975-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1d975-117">-AutomationAccountName</span></span>
<span data-ttu-id="1d975-118">指定此 Cmdlet 為其檢索憑證的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="1d975-118">Specifies the name of the Automation account for which this cmdlet retrieves a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d975-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d975-119">-DefaultProfile</span></span>
<span data-ttu-id="1d975-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="1d975-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d975-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="1d975-121">-Name</span></span>
<span data-ttu-id="1d975-122">指定要檢索之憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="1d975-122">Specifies the name of a certificate to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: ByCertificateName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d975-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d975-123">-ResourceGroupName</span></span>
<span data-ttu-id="1d975-124">指定此 Cmdlet 取得自動化憑證之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1d975-124">Specifies the name of a resource group for which this cmdlet gets an Automation certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d975-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d975-125">CommonParameters</span></span>
<span data-ttu-id="1d975-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1d975-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d975-127">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1d975-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d975-128">輸入</span><span class="sxs-lookup"><span data-stu-id="1d975-128">INPUTS</span></span>

### <span data-ttu-id="1d975-129">System.object</span><span class="sxs-lookup"><span data-stu-id="1d975-129">System.String</span></span>

## <span data-ttu-id="1d975-130">輸出</span><span class="sxs-lookup"><span data-stu-id="1d975-130">OUTPUTS</span></span>

### <span data-ttu-id="1d975-131">CertificateInfo 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1d975-131">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="1d975-132">筆記</span><span class="sxs-lookup"><span data-stu-id="1d975-132">NOTES</span></span>

## <span data-ttu-id="1d975-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="1d975-133">RELATED LINKS</span></span>

[<span data-ttu-id="1d975-134">新-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="1d975-134">New-AzAutomationCertificate</span></span>](./New-AzAutomationCertificate.md)

[<span data-ttu-id="1d975-135">移除-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="1d975-135">Remove-AzAutomationCertificate</span></span>](./Remove-AzAutomationCertificate.md)

[<span data-ttu-id="1d975-136">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="1d975-136">Set-AzAutomationCertificate</span></span>](./Set-AzAutomationCertificate.md)


