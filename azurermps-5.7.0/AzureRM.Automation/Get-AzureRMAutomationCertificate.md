---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D690C903-A481-45F2-9D42-1CE2F4184A98
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationCertificate.md
ms.openlocfilehash: 012eb357b6d64964c2564dca51ac0b77a5f96880
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446571"
---
# <span data-ttu-id="2428d-101">Get-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="2428d-101">Get-AzureRmAutomationCertificate</span></span>

## <span data-ttu-id="2428d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2428d-102">SYNOPSIS</span></span>
<span data-ttu-id="2428d-103">取得自動化憑證。</span><span class="sxs-lookup"><span data-stu-id="2428d-103">Gets Automation certificates.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2428d-104">句法</span><span class="sxs-lookup"><span data-stu-id="2428d-104">SYNTAX</span></span>

### <span data-ttu-id="2428d-105">ByAll (預設) </span><span class="sxs-lookup"><span data-stu-id="2428d-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationCertificate [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2428d-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="2428d-106">ByCertificateName</span></span>
```
Get-AzureRmAutomationCertificate [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2428d-107">說明</span><span class="sxs-lookup"><span data-stu-id="2428d-107">DESCRIPTION</span></span>
<span data-ttu-id="2428d-108">**AzureRmAutomationCertificate** Cmdlet 會取得一或多個 Azure 自動化憑證。</span><span class="sxs-lookup"><span data-stu-id="2428d-108">The **Get-AzureRmAutomationCertificate** cmdlet gets one or more Azure Automation certificates.</span></span>
<span data-ttu-id="2428d-109">根據預設，這個 Cmdlet 會取得所有憑證。</span><span class="sxs-lookup"><span data-stu-id="2428d-109">By default, this cmdlet gets all certificates.</span></span>
<span data-ttu-id="2428d-110">指定要取得特定憑證的憑證名稱。</span><span class="sxs-lookup"><span data-stu-id="2428d-110">Specify the name of a certificate to get a specific certificate.</span></span>

## <span data-ttu-id="2428d-111">示例</span><span class="sxs-lookup"><span data-stu-id="2428d-111">EXAMPLES</span></span>

### <span data-ttu-id="2428d-112">範例1：取得所有憑證</span><span class="sxs-lookup"><span data-stu-id="2428d-112">Example 1: Get all certificates</span></span>
```
PS C:\>Get-AzureRmAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="2428d-113">這個命令會針對自動化帳戶中名為 Contoso17 的所有憑證取得中繼資料。</span><span class="sxs-lookup"><span data-stu-id="2428d-113">This command gets metadata for all certificates in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="2428d-114">範例2：取得憑證</span><span class="sxs-lookup"><span data-stu-id="2428d-114">Example 2: Get a certificate</span></span>
```
PS C:\>Get-AzureRmAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17" -Name "ContosoCertificate"
```

<span data-ttu-id="2428d-115">這個命令會取得名為 ContosoCertificate 的憑證的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="2428d-115">This command gets metadata for the certificate named ContosoCertificate.</span></span>

## <span data-ttu-id="2428d-116">參數</span><span class="sxs-lookup"><span data-stu-id="2428d-116">PARAMETERS</span></span>

### <span data-ttu-id="2428d-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2428d-117">-AutomationAccountName</span></span>
<span data-ttu-id="2428d-118">指定此 Cmdlet 為其檢索憑證的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="2428d-118">Specifies the name of the Automation account for which this cmdlet retrieves a certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2428d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2428d-119">-DefaultProfile</span></span>
<span data-ttu-id="2428d-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="2428d-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2428d-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="2428d-121">-Name</span></span>
<span data-ttu-id="2428d-122">指定要檢索之憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="2428d-122">Specifies the name of a certificate to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: ByCertificateName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2428d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2428d-123">-ResourceGroupName</span></span>
<span data-ttu-id="2428d-124">指定此 Cmdlet 取得自動化憑證之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2428d-124">Specifies the name of a resource group for which this cmdlet gets an Automation certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2428d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2428d-125">CommonParameters</span></span>
<span data-ttu-id="2428d-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2428d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2428d-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2428d-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2428d-128">輸入</span><span class="sxs-lookup"><span data-stu-id="2428d-128">INPUTS</span></span>

### <span data-ttu-id="2428d-129">所有</span><span class="sxs-lookup"><span data-stu-id="2428d-129">None</span></span>
<span data-ttu-id="2428d-130">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="2428d-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2428d-131">輸出</span><span class="sxs-lookup"><span data-stu-id="2428d-131">OUTPUTS</span></span>

### <span data-ttu-id="2428d-132">CertificateInfo 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2428d-132">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="2428d-133">筆記</span><span class="sxs-lookup"><span data-stu-id="2428d-133">NOTES</span></span>

## <span data-ttu-id="2428d-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="2428d-134">RELATED LINKS</span></span>

[<span data-ttu-id="2428d-135">新-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="2428d-135">New-AzureRmAutomationCertificate</span></span>](./New-AzureRMAutomationCertificate.md)

[<span data-ttu-id="2428d-136">移除-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="2428d-136">Remove-AzureRmAutomationCertificate</span></span>](./Remove-AzureRMAutomationCertificate.md)

[<span data-ttu-id="2428d-137">Set-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="2428d-137">Set-AzureRmAutomationCertificate</span></span>](./Set-AzureRMAutomationCertificate.md)

