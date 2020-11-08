---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A504099E-BA96-45C9-A7A6-195E7087A0D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCertificate.md
ms.openlocfilehash: c80eb16f840fb6d590c139a6ec4b30d73584b741
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969387"
---
# <span data-ttu-id="1c13f-101">New-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="1c13f-101">New-AzAutomationCertificate</span></span>

## <span data-ttu-id="1c13f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1c13f-102">SYNOPSIS</span></span>
<span data-ttu-id="1c13f-103">建立自動化憑證。</span><span class="sxs-lookup"><span data-stu-id="1c13f-103">Creates an Automation certificate.</span></span>

## <span data-ttu-id="1c13f-104">句法</span><span class="sxs-lookup"><span data-stu-id="1c13f-104">SYNTAX</span></span>

```
New-AzAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path] <String> [-Exportable] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c13f-105">說明</span><span class="sxs-lookup"><span data-stu-id="1c13f-105">DESCRIPTION</span></span>
<span data-ttu-id="1c13f-106">**新的 AzAutomationCertificate** Cmdlet 會在 Azure 自動化中建立憑證。</span><span class="sxs-lookup"><span data-stu-id="1c13f-106">The **New-AzAutomationCertificate** cmdlet creates a certificate in Azure Automation.</span></span>
<span data-ttu-id="1c13f-107">提供要上傳的憑證檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="1c13f-107">Provide the path to a certificate file to upload.</span></span>

## <span data-ttu-id="1c13f-108">示例</span><span class="sxs-lookup"><span data-stu-id="1c13f-108">EXAMPLES</span></span>

### <span data-ttu-id="1c13f-109">範例1：建立新的憑證</span><span class="sxs-lookup"><span data-stu-id="1c13f-109">Example 1: Create a new certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> New-AzAutomationCertificate -AutomationAccountName "Contoso17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="1c13f-110">使用 ConvertTo-SecureString Cmdlet，第一個命令會將純文字密碼轉換為安全字串。</span><span class="sxs-lookup"><span data-stu-id="1c13f-110">The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="1c13f-111">該命令會將該物件儲存在 $Password 變數中。</span><span class="sxs-lookup"><span data-stu-id="1c13f-111">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="1c13f-112">第二個命令會建立名為 ContosoCertificate 的憑證。</span><span class="sxs-lookup"><span data-stu-id="1c13f-112">The second command creates a certificate named ContosoCertificate.</span></span>
<span data-ttu-id="1c13f-113">命令會使用儲存在 $Password 中的密碼。</span><span class="sxs-lookup"><span data-stu-id="1c13f-113">The command uses the password stored in $Password.</span></span>
<span data-ttu-id="1c13f-114">該命令會指定帳戶名稱以及它上傳檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="1c13f-114">The command specifies the account name and the path of the file that it uploads.</span></span>

## <span data-ttu-id="1c13f-115">參數</span><span class="sxs-lookup"><span data-stu-id="1c13f-115">PARAMETERS</span></span>

### <span data-ttu-id="1c13f-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1c13f-116">-AutomationAccountName</span></span>
<span data-ttu-id="1c13f-117">指定此 Cmdlet 儲存憑證的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="1c13f-117">Specifies the name of the Automation account for which this cmdlet stores the certificate.</span></span>

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

### <span data-ttu-id="1c13f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c13f-118">-DefaultProfile</span></span>
<span data-ttu-id="1c13f-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="1c13f-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1c13f-120">-描述</span><span class="sxs-lookup"><span data-stu-id="1c13f-120">-Description</span></span>
<span data-ttu-id="1c13f-121">指定憑證的描述。</span><span class="sxs-lookup"><span data-stu-id="1c13f-121">Specifies a description for the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c13f-122">匯出</span><span class="sxs-lookup"><span data-stu-id="1c13f-122">-Exportable</span></span>
<span data-ttu-id="1c13f-123">指定是否可以匯出證書。</span><span class="sxs-lookup"><span data-stu-id="1c13f-123">Specifies whether the certificate can be exported.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c13f-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="1c13f-124">-Name</span></span>
<span data-ttu-id="1c13f-125">指定憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="1c13f-125">Specifies the name for the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c13f-126">-Password</span><span class="sxs-lookup"><span data-stu-id="1c13f-126">-Password</span></span>
<span data-ttu-id="1c13f-127">指定憑證檔的密碼。</span><span class="sxs-lookup"><span data-stu-id="1c13f-127">Specifies the password for the certificate file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c13f-128">-Path</span><span class="sxs-lookup"><span data-stu-id="1c13f-128">-Path</span></span>
<span data-ttu-id="1c13f-129">指定此 Cmdlet 上傳的腳本檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="1c13f-129">Specifies the path to a script file that this cmdlet uploads.</span></span>
<span data-ttu-id="1c13f-130">檔案可以是 .cer 或 .pfx 檔案。</span><span class="sxs-lookup"><span data-stu-id="1c13f-130">The file can be a .cer or a .pfx file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c13f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c13f-131">-ResourceGroupName</span></span>
<span data-ttu-id="1c13f-132">指定此 Cmdlet 為其建立憑證的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1c13f-132">Specifies the name of the resource group for which this cmdlet creates a certificate.</span></span>

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

### <span data-ttu-id="1c13f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c13f-133">CommonParameters</span></span>
<span data-ttu-id="1c13f-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1c13f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c13f-135">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1c13f-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c13f-136">輸入</span><span class="sxs-lookup"><span data-stu-id="1c13f-136">INPUTS</span></span>

### <span data-ttu-id="1c13f-137">System.object</span><span class="sxs-lookup"><span data-stu-id="1c13f-137">System.String</span></span>

### <span data-ttu-id="1c13f-138">SecureString</span><span class="sxs-lookup"><span data-stu-id="1c13f-138">System.Security.SecureString</span></span>

### <span data-ttu-id="1c13f-139">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="1c13f-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1c13f-140">輸出</span><span class="sxs-lookup"><span data-stu-id="1c13f-140">OUTPUTS</span></span>

### <span data-ttu-id="1c13f-141">CertificateInfo 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1c13f-141">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="1c13f-142">筆記</span><span class="sxs-lookup"><span data-stu-id="1c13f-142">NOTES</span></span>

<span data-ttu-id="1c13f-143">這個命令應該在您是系統管理員的電腦上執行，以及在提升的 PowerShell 會話中執行;在上傳憑證前，此 Cmdlet 會使用 local x.509 store 來檢索指紋和金鑰，如果此 Cmdlet 是在提升的 PowerShell 會話之外執行，您會收到「拒絕存取」錯誤。</span><span class="sxs-lookup"><span data-stu-id="1c13f-143">This command should be run on a machine that you are an administrator of, as well as in an elevated PowerShell session; before the certificate is uploaded, this cmdlet uses the local X.509 store to retrieve the thumbprint and key, and if this cmdlet is run outside of an elevated PowerShell session, you will receive an "Access denied" error.</span></span>

## <span data-ttu-id="1c13f-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="1c13f-144">RELATED LINKS</span></span>

[<span data-ttu-id="1c13f-145">AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="1c13f-145">Get-AzAutomationCertificate</span></span>](./Get-AzAutomationCertificate.md)

[<span data-ttu-id="1c13f-146">移除-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="1c13f-146">Remove-AzAutomationCertificate</span></span>](./Remove-AzAutomationCertificate.md)

[<span data-ttu-id="1c13f-147">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="1c13f-147">Set-AzAutomationCertificate</span></span>](./Set-AzAutomationCertificate.md)


