---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D690C903-A481-45F2-9D42-1CE2F4184A98
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCertificate.md
ms.openlocfilehash: 1680f4080f0e3def2e18d90273ce9e6f2f6d0bcb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912502"
---
# <span data-ttu-id="caf1d-101">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="caf1d-101">Get-AzAutomationCertificate</span></span>

## <span data-ttu-id="caf1d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="caf1d-102">SYNOPSIS</span></span>
<span data-ttu-id="caf1d-103">獲得自動化憑證。</span><span class="sxs-lookup"><span data-stu-id="caf1d-103">Gets Automation certificates.</span></span>

## <span data-ttu-id="caf1d-104">語法</span><span class="sxs-lookup"><span data-stu-id="caf1d-104">SYNTAX</span></span>

### <span data-ttu-id="caf1d-105">根據預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="caf1d-105">ByAll (Default)</span></span>
```
Get-AzAutomationCertificate [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="caf1d-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="caf1d-106">ByCertificateName</span></span>
```
Get-AzAutomationCertificate [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="caf1d-107">描述</span><span class="sxs-lookup"><span data-stu-id="caf1d-107">DESCRIPTION</span></span>
<span data-ttu-id="caf1d-108">**Get-AzAutomationCertificate** Cmdlet 會取得一或多個 Azure 自動化憑證。</span><span class="sxs-lookup"><span data-stu-id="caf1d-108">The **Get-AzAutomationCertificate** cmdlet gets one or more Azure Automation certificates.</span></span>
<span data-ttu-id="caf1d-109">根據預設，此 Cmdlet 會獲得所有憑證。</span><span class="sxs-lookup"><span data-stu-id="caf1d-109">By default, this cmdlet gets all certificates.</span></span>
<span data-ttu-id="caf1d-110">指定憑證的名稱以取得特定憑證。</span><span class="sxs-lookup"><span data-stu-id="caf1d-110">Specify the name of a certificate to get a specific certificate.</span></span>

## <span data-ttu-id="caf1d-111">例子</span><span class="sxs-lookup"><span data-stu-id="caf1d-111">EXAMPLES</span></span>

### <span data-ttu-id="caf1d-112">範例 1：取得所有憑證</span><span class="sxs-lookup"><span data-stu-id="caf1d-112">Example 1: Get all certificates</span></span>
```
PS C:\>Get-AzAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="caf1d-113">此命令會獲得自動化帳戶中所有憑證的中繼資料，名稱為 Contoso17。</span><span class="sxs-lookup"><span data-stu-id="caf1d-113">This command gets metadata for all certificates in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="caf1d-114">範例 2：取得憑證</span><span class="sxs-lookup"><span data-stu-id="caf1d-114">Example 2: Get a certificate</span></span>
```
PS C:\>Get-AzAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17" -Name "ContosoCertificate"
```

<span data-ttu-id="caf1d-115">此命令會獲得名稱為 ContosoCertificate 之憑證的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="caf1d-115">This command gets metadata for the certificate named ContosoCertificate.</span></span>

## <span data-ttu-id="caf1d-116">參數</span><span class="sxs-lookup"><span data-stu-id="caf1d-116">PARAMETERS</span></span>

### <span data-ttu-id="caf1d-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="caf1d-117">-AutomationAccountName</span></span>
<span data-ttu-id="caf1d-118">指定此 Cmdlet 所取取憑證的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="caf1d-118">Specifies the name of the Automation account for which this cmdlet retrieves a certificate.</span></span>

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

### <span data-ttu-id="caf1d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="caf1d-119">-DefaultProfile</span></span>
<span data-ttu-id="caf1d-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="caf1d-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="caf1d-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="caf1d-121">-Name</span></span>
<span data-ttu-id="caf1d-122">指定要取回的憑證名稱。</span><span class="sxs-lookup"><span data-stu-id="caf1d-122">Specifies the name of a certificate to retrieve.</span></span>

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

### <span data-ttu-id="caf1d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="caf1d-123">-ResourceGroupName</span></span>
<span data-ttu-id="caf1d-124">指定此 Cmdlet 會獲得自動化憑證的資源組名。</span><span class="sxs-lookup"><span data-stu-id="caf1d-124">Specifies the name of a resource group for which this cmdlet gets an Automation certificate.</span></span>

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

### <span data-ttu-id="caf1d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="caf1d-125">CommonParameters</span></span>
<span data-ttu-id="caf1d-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="caf1d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="caf1d-127">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="caf1d-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="caf1d-128">輸入</span><span class="sxs-lookup"><span data-stu-id="caf1d-128">INPUTS</span></span>

### <span data-ttu-id="caf1d-129">System.String</span><span class="sxs-lookup"><span data-stu-id="caf1d-129">System.String</span></span>

## <span data-ttu-id="caf1d-130">輸出</span><span class="sxs-lookup"><span data-stu-id="caf1d-130">OUTPUTS</span></span>

### <span data-ttu-id="caf1d-131">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="caf1d-131">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="caf1d-132">筆記</span><span class="sxs-lookup"><span data-stu-id="caf1d-132">NOTES</span></span>

## <span data-ttu-id="caf1d-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="caf1d-133">RELATED LINKS</span></span>

[<span data-ttu-id="caf1d-134">New-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="caf1d-134">New-AzAutomationCertificate</span></span>](./New-AzAutomationCertificate.md)

[<span data-ttu-id="caf1d-135">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="caf1d-135">Remove-AzAutomationCertificate</span></span>](./Remove-AzAutomationCertificate.md)

[<span data-ttu-id="caf1d-136">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="caf1d-136">Set-AzAutomationCertificate</span></span>](./Set-AzAutomationCertificate.md)


