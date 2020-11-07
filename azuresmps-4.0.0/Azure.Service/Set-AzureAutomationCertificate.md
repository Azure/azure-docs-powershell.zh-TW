---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: AE74024A-A12A-4EC4-AF6C-62F921EA2532
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6b19d0bb0c95e9d489fe26c1cd74705318cedcf2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967874"
---
# <span data-ttu-id="5d1e7-101">Set-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="5d1e7-101">Set-AzureAutomationCertificate</span></span>

## <span data-ttu-id="5d1e7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5d1e7-102">SYNOPSIS</span></span>

<span data-ttu-id="5d1e7-103">修改自動化憑證的設定。</span><span class="sxs-lookup"><span data-stu-id="5d1e7-103">Modifies the configuration of an Automation certificate.</span></span>

## <span data-ttu-id="5d1e7-104">句法</span><span class="sxs-lookup"><span data-stu-id="5d1e7-104">SYNTAX</span></span>

```
Set-AzureAutomationCertificate -Name <String> [-Description <String>] [-Password <SecureString>]
 [-Path <String>] [-Exportable <Boolean>] -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="5d1e7-105">說明</span><span class="sxs-lookup"><span data-stu-id="5d1e7-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="5d1e7-106">AzureAutomationCertificate Cmdlet 會修改 Microsoft Azure 自動化中的憑證 **設定** 。</span><span class="sxs-lookup"><span data-stu-id="5d1e7-106">The **Set-AzureAutomationCertificate** cmdlet modifies the configuration of a certificate in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="5d1e7-107">示例</span><span class="sxs-lookup"><span data-stu-id="5d1e7-107">EXAMPLES</span></span>

### <span data-ttu-id="5d1e7-108">範例1：更新憑證</span><span class="sxs-lookup"><span data-stu-id="5d1e7-108">Example 1: Update a certificate</span></span>
```
PS C:\> $password = ConvertTo-SecureString "PassWord!" -AsPlainText -Force
PS C:\> Set-AzureAutomationCertificate -AutomationAccountName "Contos17" -Name "MyCertificate" -Path "./cert.pfx" -Password $password
```

<span data-ttu-id="5d1e7-109">這些命令會在自動化中更新名為 MyCertificate 的現有證書。</span><span class="sxs-lookup"><span data-stu-id="5d1e7-109">These commands update an existing certificate named MyCertificate in Automation.</span></span>
<span data-ttu-id="5d1e7-110">第一個命令會針對更新憑證之第二個命令中所用的憑證檔案建立密碼。</span><span class="sxs-lookup"><span data-stu-id="5d1e7-110">The first command creates the password for the certificate file that is used in the second command that updates the certificate.</span></span>

## <span data-ttu-id="5d1e7-111">參數</span><span class="sxs-lookup"><span data-stu-id="5d1e7-111">PARAMETERS</span></span>

### <span data-ttu-id="5d1e7-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5d1e7-112">-AutomationAccountName</span></span>
<span data-ttu-id="5d1e7-113">指定憑證的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="5d1e7-113">Specifies the name of the Automation account with the certificate.</span></span>

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

### <span data-ttu-id="5d1e7-114">-描述</span><span class="sxs-lookup"><span data-stu-id="5d1e7-114">-Description</span></span>
<span data-ttu-id="5d1e7-115">指定憑證的描述。</span><span class="sxs-lookup"><span data-stu-id="5d1e7-115">Specifies a description for the certificate.</span></span>

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

### <span data-ttu-id="5d1e7-116">匯出</span><span class="sxs-lookup"><span data-stu-id="5d1e7-116">-Exportable</span></span>
<span data-ttu-id="5d1e7-117">表示可以匯出的憑證。</span><span class="sxs-lookup"><span data-stu-id="5d1e7-117">Indicates the certificate can be exported.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d1e7-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="5d1e7-118">-Name</span></span>
<span data-ttu-id="5d1e7-119">指定憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="5d1e7-119">Specifies the name of the certificate.</span></span>

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

### <span data-ttu-id="5d1e7-120">-Password</span><span class="sxs-lookup"><span data-stu-id="5d1e7-120">-Password</span></span>
<span data-ttu-id="5d1e7-121">指定憑證檔的密碼。</span><span class="sxs-lookup"><span data-stu-id="5d1e7-121">Specifies the password for the certificate file.</span></span>

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

### <span data-ttu-id="5d1e7-122">-Path</span><span class="sxs-lookup"><span data-stu-id="5d1e7-122">-Path</span></span>
<span data-ttu-id="5d1e7-123">指定要上傳的腳本檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="5d1e7-123">Specifies the path to a script file to upload.</span></span>
<span data-ttu-id="5d1e7-124">檔案可以是 .cer 或 .pfx。</span><span class="sxs-lookup"><span data-stu-id="5d1e7-124">The file can be .cer or .pfx.</span></span>

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

### <span data-ttu-id="5d1e7-125">-設定檔</span><span class="sxs-lookup"><span data-stu-id="5d1e7-125">-Profile</span></span>
<span data-ttu-id="5d1e7-126">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="5d1e7-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5d1e7-127">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="5d1e7-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5d1e7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d1e7-128">CommonParameters</span></span>
<span data-ttu-id="5d1e7-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5d1e7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d1e7-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5d1e7-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d1e7-131">輸入</span><span class="sxs-lookup"><span data-stu-id="5d1e7-131">INPUTS</span></span>

## <span data-ttu-id="5d1e7-132">輸出</span><span class="sxs-lookup"><span data-stu-id="5d1e7-132">OUTPUTS</span></span>

### <span data-ttu-id="5d1e7-133">CertificateInfo 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="5d1e7-133">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="5d1e7-134">筆記</span><span class="sxs-lookup"><span data-stu-id="5d1e7-134">NOTES</span></span>

## <span data-ttu-id="5d1e7-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="5d1e7-135">RELATED LINKS</span></span>

[<span data-ttu-id="5d1e7-136">AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="5d1e7-136">Get-AzureAutomationCertificate</span></span>](./Get-AzureAutomationCertificate.md)

[<span data-ttu-id="5d1e7-137">新-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="5d1e7-137">New-AzureAutomationCertificate</span></span>](./New-AzureAutomationCertificate.md)

[<span data-ttu-id="5d1e7-138">移除-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="5d1e7-138">Remove-AzureAutomationCertificate</span></span>](./Remove-AzureAutomationCertificate.md)


