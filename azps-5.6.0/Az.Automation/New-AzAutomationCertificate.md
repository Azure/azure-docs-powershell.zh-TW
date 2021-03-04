---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A504099E-BA96-45C9-A7A6-195E7087A0D4
online version: https://docs.microsoft.com/powershell/module/az.automation/new-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCertificate.md
ms.openlocfilehash: 3f92ebfcb9b768788b0a9acd7a1e11ef766fd22b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916789"
---
# <span data-ttu-id="eb46b-101">New-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="eb46b-101">New-AzAutomationCertificate</span></span>

## <span data-ttu-id="eb46b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="eb46b-102">SYNOPSIS</span></span>
<span data-ttu-id="eb46b-103">建立自動化憑證。</span><span class="sxs-lookup"><span data-stu-id="eb46b-103">Creates an Automation certificate.</span></span>

## <span data-ttu-id="eb46b-104">語法</span><span class="sxs-lookup"><span data-stu-id="eb46b-104">SYNTAX</span></span>

```
New-AzAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path] <String> [-Exportable] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb46b-105">描述</span><span class="sxs-lookup"><span data-stu-id="eb46b-105">DESCRIPTION</span></span>
<span data-ttu-id="eb46b-106">**New-AzAutomationCertificate** Cmdlet 在 Azure Automation 中建立憑證。</span><span class="sxs-lookup"><span data-stu-id="eb46b-106">The **New-AzAutomationCertificate** cmdlet creates a certificate in Azure Automation.</span></span>
<span data-ttu-id="eb46b-107">提供要上傳之憑證檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="eb46b-107">Provide the path to a certificate file to upload.</span></span>

## <span data-ttu-id="eb46b-108">例子</span><span class="sxs-lookup"><span data-stu-id="eb46b-108">EXAMPLES</span></span>

### <span data-ttu-id="eb46b-109">範例 1：建立新憑證</span><span class="sxs-lookup"><span data-stu-id="eb46b-109">Example 1: Create a new certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> New-AzAutomationCertificate -AutomationAccountName "Contoso17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="eb46b-110">第一個命令會使用 Cmdlet 將純文字密碼轉換為ConvertTo-SecureString字串。</span><span class="sxs-lookup"><span data-stu-id="eb46b-110">The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="eb46b-111">該命令將該物件儲存在$Password變數中。</span><span class="sxs-lookup"><span data-stu-id="eb46b-111">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="eb46b-112">第二個命令會建立名為 ContosoCertificate 的憑證。</span><span class="sxs-lookup"><span data-stu-id="eb46b-112">The second command creates a certificate named ContosoCertificate.</span></span>
<span data-ttu-id="eb46b-113">命令使用儲存在 $Password。</span><span class="sxs-lookup"><span data-stu-id="eb46b-113">The command uses the password stored in $Password.</span></span>
<span data-ttu-id="eb46b-114">命令會指定帳戶名稱及其上傳之檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="eb46b-114">The command specifies the account name and the path of the file that it uploads.</span></span>

## <span data-ttu-id="eb46b-115">參數</span><span class="sxs-lookup"><span data-stu-id="eb46b-115">PARAMETERS</span></span>

### <span data-ttu-id="eb46b-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="eb46b-116">-AutomationAccountName</span></span>
<span data-ttu-id="eb46b-117">指定此 Cmdlet 儲存憑證的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="eb46b-117">Specifies the name of the Automation account for which this cmdlet stores the certificate.</span></span>

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

### <span data-ttu-id="eb46b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb46b-118">-DefaultProfile</span></span>
<span data-ttu-id="eb46b-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="eb46b-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eb46b-120">-描述</span><span class="sxs-lookup"><span data-stu-id="eb46b-120">-Description</span></span>
<span data-ttu-id="eb46b-121">指定憑證的描述。</span><span class="sxs-lookup"><span data-stu-id="eb46b-121">Specifies a description for the certificate.</span></span>

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

### <span data-ttu-id="eb46b-122">-可匯出</span><span class="sxs-lookup"><span data-stu-id="eb46b-122">-Exportable</span></span>
<span data-ttu-id="eb46b-123">指定是否可以匯出憑證。</span><span class="sxs-lookup"><span data-stu-id="eb46b-123">Specifies whether the certificate can be exported.</span></span>

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

### <span data-ttu-id="eb46b-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="eb46b-124">-Name</span></span>
<span data-ttu-id="eb46b-125">指定憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="eb46b-125">Specifies the name for the certificate.</span></span>

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

### <span data-ttu-id="eb46b-126">-密碼</span><span class="sxs-lookup"><span data-stu-id="eb46b-126">-Password</span></span>
<span data-ttu-id="eb46b-127">指定憑證檔案的密碼。</span><span class="sxs-lookup"><span data-stu-id="eb46b-127">Specifies the password for the certificate file.</span></span>

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

### <span data-ttu-id="eb46b-128">-路徑</span><span class="sxs-lookup"><span data-stu-id="eb46b-128">-Path</span></span>
<span data-ttu-id="eb46b-129">指定此 Cmdlet 上傳之腳本檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="eb46b-129">Specifies the path to a script file that this cmdlet uploads.</span></span>
<span data-ttu-id="eb46b-130">檔案可以是 .cer 或 .pfx 檔案。</span><span class="sxs-lookup"><span data-stu-id="eb46b-130">The file can be a .cer or a .pfx file.</span></span>

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

### <span data-ttu-id="eb46b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb46b-131">-ResourceGroupName</span></span>
<span data-ttu-id="eb46b-132">指定此 Cmdlet 建立憑證的資源組名。</span><span class="sxs-lookup"><span data-stu-id="eb46b-132">Specifies the name of the resource group for which this cmdlet creates a certificate.</span></span>

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

### <span data-ttu-id="eb46b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb46b-133">CommonParameters</span></span>
<span data-ttu-id="eb46b-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="eb46b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb46b-135">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="eb46b-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb46b-136">輸入</span><span class="sxs-lookup"><span data-stu-id="eb46b-136">INPUTS</span></span>

### <span data-ttu-id="eb46b-137">System.String</span><span class="sxs-lookup"><span data-stu-id="eb46b-137">System.String</span></span>

### <span data-ttu-id="eb46b-138">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="eb46b-138">System.Security.SecureString</span></span>

### <span data-ttu-id="eb46b-139">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="eb46b-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="eb46b-140">輸出</span><span class="sxs-lookup"><span data-stu-id="eb46b-140">OUTPUTS</span></span>

### <span data-ttu-id="eb46b-141">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="eb46b-141">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="eb46b-142">筆記</span><span class="sxs-lookup"><span data-stu-id="eb46b-142">NOTES</span></span>

<span data-ttu-id="eb46b-143">此命令應執行于您擔任系統管理員的一部電腦上，以及提升許可權的 PowerShell 會話中;上傳憑證之前，此 Cmdlet 會使用本地 X.509 存放區來取回指紋和金鑰，如果此 Cmdlet 是在提升許可權的 PowerShell 會話之外執行，您會收到「拒絕存取」錯誤。</span><span class="sxs-lookup"><span data-stu-id="eb46b-143">This command should be run on a machine that you are an administrator of, as well as in an elevated PowerShell session; before the certificate is uploaded, this cmdlet uses the local X.509 store to retrieve the thumbprint and key, and if this cmdlet is run outside of an elevated PowerShell session, you will receive an "Access denied" error.</span></span>

## <span data-ttu-id="eb46b-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="eb46b-144">RELATED LINKS</span></span>

[<span data-ttu-id="eb46b-145">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="eb46b-145">Get-AzAutomationCertificate</span></span>](./Get-AzAutomationCertificate.md)

[<span data-ttu-id="eb46b-146">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="eb46b-146">Remove-AzAutomationCertificate</span></span>](./Remove-AzAutomationCertificate.md)

[<span data-ttu-id="eb46b-147">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="eb46b-147">Set-AzAutomationCertificate</span></span>](./Set-AzAutomationCertificate.md)


