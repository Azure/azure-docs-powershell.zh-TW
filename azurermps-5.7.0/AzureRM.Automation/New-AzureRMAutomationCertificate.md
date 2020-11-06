---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: A504099E-BA96-45C9-A7A6-195E7087A0D4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationCertificate.md
ms.openlocfilehash: e82d78254e81a5b8fb98c1dfbfac2113d19361a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444784"
---
# <span data-ttu-id="6eacf-101">New-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="6eacf-101">New-AzureRmAutomationCertificate</span></span>

## <span data-ttu-id="6eacf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6eacf-102">SYNOPSIS</span></span>
<span data-ttu-id="6eacf-103">建立自動化憑證。</span><span class="sxs-lookup"><span data-stu-id="6eacf-103">Creates an Automation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6eacf-104">句法</span><span class="sxs-lookup"><span data-stu-id="6eacf-104">SYNTAX</span></span>

```
New-AzureRmAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path] <String> [-Exportable] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6eacf-105">說明</span><span class="sxs-lookup"><span data-stu-id="6eacf-105">DESCRIPTION</span></span>
<span data-ttu-id="6eacf-106">**新的 AzureRmAutomationCertificate** Cmdlet 會在 Azure 自動化中建立憑證。</span><span class="sxs-lookup"><span data-stu-id="6eacf-106">The **New-AzureRmAutomationCertificate** cmdlet creates a certificate in Azure Automation.</span></span>
<span data-ttu-id="6eacf-107">提供要上傳的憑證檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="6eacf-107">Provide the path to a certificate file to upload.</span></span>

## <span data-ttu-id="6eacf-108">示例</span><span class="sxs-lookup"><span data-stu-id="6eacf-108">EXAMPLES</span></span>

### <span data-ttu-id="6eacf-109">範例1：建立新的憑證</span><span class="sxs-lookup"><span data-stu-id="6eacf-109">Example 1: Create a new certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> New-AzureRmAutomationCertificate -AutomationAccountName "Contoso17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="6eacf-110">使用 ConvertTo-SecureString Cmdlet，第一個命令會將純文字密碼轉換為安全字串。</span><span class="sxs-lookup"><span data-stu-id="6eacf-110">The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="6eacf-111">該命令會將該物件儲存在 $Password 變數中。</span><span class="sxs-lookup"><span data-stu-id="6eacf-111">The command stores that object in the $Password variable.</span></span>

<span data-ttu-id="6eacf-112">第二個命令會建立名為 ContosoCertificate 的憑證。</span><span class="sxs-lookup"><span data-stu-id="6eacf-112">The second command creates a certificate named ContosoCertificate.</span></span>
<span data-ttu-id="6eacf-113">命令會使用儲存在 $Password 中的密碼。</span><span class="sxs-lookup"><span data-stu-id="6eacf-113">The command uses the password stored in $Password.</span></span>
<span data-ttu-id="6eacf-114">該命令會指定帳戶名稱以及它上傳檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="6eacf-114">The command specifies the account name and the path of the file that it uploads.</span></span>

## <span data-ttu-id="6eacf-115">參數</span><span class="sxs-lookup"><span data-stu-id="6eacf-115">PARAMETERS</span></span>

### <span data-ttu-id="6eacf-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6eacf-116">-AutomationAccountName</span></span>
<span data-ttu-id="6eacf-117">指定此 Cmdlet 儲存憑證的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="6eacf-117">Specifies the name of the Automation account for which this cmdlet stores the certificate.</span></span>

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

### <span data-ttu-id="6eacf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6eacf-118">-DefaultProfile</span></span>
<span data-ttu-id="6eacf-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="6eacf-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6eacf-120">-描述</span><span class="sxs-lookup"><span data-stu-id="6eacf-120">-Description</span></span>
<span data-ttu-id="6eacf-121">指定憑證的描述。</span><span class="sxs-lookup"><span data-stu-id="6eacf-121">Specifies a description for the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6eacf-122">匯出</span><span class="sxs-lookup"><span data-stu-id="6eacf-122">-Exportable</span></span>
<span data-ttu-id="6eacf-123">指定是否可以匯出證書。</span><span class="sxs-lookup"><span data-stu-id="6eacf-123">Specifies whether the certificate can be exported.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6eacf-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="6eacf-124">-Name</span></span>
<span data-ttu-id="6eacf-125">指定憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="6eacf-125">Specifies the name for the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6eacf-126">-Password</span><span class="sxs-lookup"><span data-stu-id="6eacf-126">-Password</span></span>
<span data-ttu-id="6eacf-127">指定憑證檔的密碼。</span><span class="sxs-lookup"><span data-stu-id="6eacf-127">Specifies the password for the certificate file.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6eacf-128">-Path</span><span class="sxs-lookup"><span data-stu-id="6eacf-128">-Path</span></span>
<span data-ttu-id="6eacf-129">指定此 Cmdlet 上傳的腳本檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="6eacf-129">Specifies the path to a script file that this cmdlet uploads.</span></span>
<span data-ttu-id="6eacf-130">檔案可以是 .cer 或 .pfx 檔案。</span><span class="sxs-lookup"><span data-stu-id="6eacf-130">The file can be a .cer or a .pfx file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6eacf-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6eacf-131">-ResourceGroupName</span></span>
<span data-ttu-id="6eacf-132">指定此 Cmdlet 為其建立憑證的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6eacf-132">Specifies the name of the resource group for which this cmdlet creates a certificate.</span></span>

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

### <span data-ttu-id="6eacf-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6eacf-133">CommonParameters</span></span>
<span data-ttu-id="6eacf-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6eacf-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6eacf-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6eacf-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6eacf-136">輸入</span><span class="sxs-lookup"><span data-stu-id="6eacf-136">INPUTS</span></span>

### <span data-ttu-id="6eacf-137">所有</span><span class="sxs-lookup"><span data-stu-id="6eacf-137">None</span></span>
<span data-ttu-id="6eacf-138">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="6eacf-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6eacf-139">輸出</span><span class="sxs-lookup"><span data-stu-id="6eacf-139">OUTPUTS</span></span>

### <span data-ttu-id="6eacf-140">CertificateInfo 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6eacf-140">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="6eacf-141">筆記</span><span class="sxs-lookup"><span data-stu-id="6eacf-141">NOTES</span></span>

## <span data-ttu-id="6eacf-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="6eacf-142">RELATED LINKS</span></span>

[<span data-ttu-id="6eacf-143">AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="6eacf-143">Get-AzureRmAutomationCertificate</span></span>](./Get-AzureRMAutomationCertificate.md)

[<span data-ttu-id="6eacf-144">移除-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="6eacf-144">Remove-AzureRmAutomationCertificate</span></span>](./Remove-AzureRMAutomationCertificate.md)

[<span data-ttu-id="6eacf-145">Set-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="6eacf-145">Set-AzureRmAutomationCertificate</span></span>](./Set-AzureRMAutomationCertificate.md)

