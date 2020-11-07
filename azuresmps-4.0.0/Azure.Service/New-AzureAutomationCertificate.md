---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: FDA8BAAA-7C37-4BCB-9C02-EB6296C09C2B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 00904cc1b67c32bc3658c1c4f6e8b123a5601ff7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967668"
---
# <span data-ttu-id="e8bb9-101">New-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="e8bb9-101">New-AzureAutomationCertificate</span></span>

## <span data-ttu-id="e8bb9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e8bb9-102">SYNOPSIS</span></span>

<span data-ttu-id="e8bb9-103">建立 Azure 自動化憑證。</span><span class="sxs-lookup"><span data-stu-id="e8bb9-103">Creates an Azure Automation certificate.</span></span>

## <span data-ttu-id="e8bb9-104">句法</span><span class="sxs-lookup"><span data-stu-id="e8bb9-104">SYNTAX</span></span>

```
New-AzureAutomationCertificate -Name <String> [-Description <String>] [-Password <SecureString>] -Path <String>
 [-Exportable] -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e8bb9-105">說明</span><span class="sxs-lookup"><span data-stu-id="e8bb9-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="e8bb9-106">**新的 AzureAutomationCertificate** Cmdlet 會在 Microsoft Azure 自動化中建立憑證。</span><span class="sxs-lookup"><span data-stu-id="e8bb9-106">The **New-AzureAutomationCertificate** cmdlet creates a certificate in Microsoft Azure Automation.</span></span>
<span data-ttu-id="e8bb9-107">您提供要上傳的憑證檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="e8bb9-107">You provide the path to a certificate file to upload.</span></span>

## <span data-ttu-id="e8bb9-108">示例</span><span class="sxs-lookup"><span data-stu-id="e8bb9-108">EXAMPLES</span></span>

### <span data-ttu-id="e8bb9-109">範例1：建立憑證</span><span class="sxs-lookup"><span data-stu-id="e8bb9-109">Example 1: Create a certificate</span></span>
```
PS C:\> $password = ConvertTo-SecureString "PassWord!" -AsPlainText -Force
PS C:\> New-AzureAutomationCertificate -AutomationAccountName "Contoso17" -Name "MyCertificate" -Path "./cert.pfx" -Password $password
```

<span data-ttu-id="e8bb9-110">這些命令會在 Azure 自動化中建立名為 MyCertificate 的憑證。</span><span class="sxs-lookup"><span data-stu-id="e8bb9-110">These commands create a certificate in Azure Automation named MyCertificate.</span></span>
<span data-ttu-id="e8bb9-111">第一個命令會建立證書檔案的密碼，該檔案是在建立憑證的第二個命令中使用的憑證檔案。</span><span class="sxs-lookup"><span data-stu-id="e8bb9-111">The first command creates the password for the certificate file that is used in the second command that creates the certificate.</span></span>

## <span data-ttu-id="e8bb9-112">參數</span><span class="sxs-lookup"><span data-stu-id="e8bb9-112">PARAMETERS</span></span>

### <span data-ttu-id="e8bb9-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e8bb9-113">-AutomationAccountName</span></span>
<span data-ttu-id="e8bb9-114">指定將儲存憑證之自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="e8bb9-114">Specifies the name of the Automation account the certificate will be stored in.</span></span>

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

### <span data-ttu-id="e8bb9-115">-描述</span><span class="sxs-lookup"><span data-stu-id="e8bb9-115">-Description</span></span>
<span data-ttu-id="e8bb9-116">指定憑證的描述。</span><span class="sxs-lookup"><span data-stu-id="e8bb9-116">Specifies a description for the certificate.</span></span>

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

### <span data-ttu-id="e8bb9-117">匯出</span><span class="sxs-lookup"><span data-stu-id="e8bb9-117">-Exportable</span></span>
<span data-ttu-id="e8bb9-118">表示可以匯出的憑證。</span><span class="sxs-lookup"><span data-stu-id="e8bb9-118">Indicates the certificate can be exported.</span></span>

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

### <span data-ttu-id="e8bb9-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="e8bb9-119">-Name</span></span>
<span data-ttu-id="e8bb9-120">指定憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="e8bb9-120">Specifies a name for the certificate.</span></span>

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

### <span data-ttu-id="e8bb9-121">-Password</span><span class="sxs-lookup"><span data-stu-id="e8bb9-121">-Password</span></span>
<span data-ttu-id="e8bb9-122">指定憑證檔的密碼。</span><span class="sxs-lookup"><span data-stu-id="e8bb9-122">Specifies the password for the certificate file.</span></span>

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

### <span data-ttu-id="e8bb9-123">-Path</span><span class="sxs-lookup"><span data-stu-id="e8bb9-123">-Path</span></span>
<span data-ttu-id="e8bb9-124">指定要上傳的腳本檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="e8bb9-124">Specifies the path to a script file to upload.</span></span>
<span data-ttu-id="e8bb9-125">檔案可以是 .cer 或 .pfx。</span><span class="sxs-lookup"><span data-stu-id="e8bb9-125">The file can be .cer or .pfx.</span></span>

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

### <span data-ttu-id="e8bb9-126">-設定檔</span><span class="sxs-lookup"><span data-stu-id="e8bb9-126">-Profile</span></span>
<span data-ttu-id="e8bb9-127">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="e8bb9-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e8bb9-128">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="e8bb9-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e8bb9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8bb9-129">CommonParameters</span></span>
<span data-ttu-id="e8bb9-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e8bb9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8bb9-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e8bb9-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8bb9-132">輸入</span><span class="sxs-lookup"><span data-stu-id="e8bb9-132">INPUTS</span></span>

## <span data-ttu-id="e8bb9-133">輸出</span><span class="sxs-lookup"><span data-stu-id="e8bb9-133">OUTPUTS</span></span>

### <span data-ttu-id="e8bb9-134">CertificateInfo 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e8bb9-134">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="e8bb9-135">筆記</span><span class="sxs-lookup"><span data-stu-id="e8bb9-135">NOTES</span></span>

## <span data-ttu-id="e8bb9-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="e8bb9-136">RELATED LINKS</span></span>

[<span data-ttu-id="e8bb9-137">AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="e8bb9-137">Get-AzureAutomationCertificate</span></span>](./Get-AzureAutomationCertificate.md)

[<span data-ttu-id="e8bb9-138">移除-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="e8bb9-138">Remove-AzureAutomationCertificate</span></span>](./Remove-AzureAutomationCertificate.md)

[<span data-ttu-id="e8bb9-139">Set-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="e8bb9-139">Set-AzureAutomationCertificate</span></span>](./Set-AzureAutomationCertificate.md)


