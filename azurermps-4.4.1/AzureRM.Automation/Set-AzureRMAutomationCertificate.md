---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: F1A2861F-14EF-4F67-8452-31FD498528BB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationCertificate.md
ms.openlocfilehash: 97a5db6a816b2274befde1d4efb898b0c5e2bfdf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457328"
---
# <span data-ttu-id="ed91e-101">Set-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="ed91e-101">Set-AzureRmAutomationCertificate</span></span>

## <span data-ttu-id="ed91e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ed91e-102">SYNOPSIS</span></span>
<span data-ttu-id="ed91e-103">修改自動化憑證的設定。</span><span class="sxs-lookup"><span data-stu-id="ed91e-103">Modifies the configuration of an Automation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed91e-104">句法</span><span class="sxs-lookup"><span data-stu-id="ed91e-104">SYNTAX</span></span>

```
Set-AzureRmAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path <String>] [-Exportable <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed91e-105">說明</span><span class="sxs-lookup"><span data-stu-id="ed91e-105">DESCRIPTION</span></span>
<span data-ttu-id="ed91e-106">AzureRmAutomationCertificate Cmdlet 會修改 Azure 自動化中憑證的 **設定** 。</span><span class="sxs-lookup"><span data-stu-id="ed91e-106">The **Set-AzureRmAutomationCertificate** cmdlet modifies the configuration of a certificate in Azure Automation.</span></span>

## <span data-ttu-id="ed91e-107">示例</span><span class="sxs-lookup"><span data-stu-id="ed91e-107">EXAMPLES</span></span>

### <span data-ttu-id="ed91e-108">範例1：修改憑證</span><span class="sxs-lookup"><span data-stu-id="ed91e-108">Example 1: Modify a certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> Set-AzureAutomationCertificate -AutomationAccountName "Contos17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="ed91e-109">使用 ConvertTo-SecureString Cmdlet，第一個命令會將純文字密碼轉換為安全字串。</span><span class="sxs-lookup"><span data-stu-id="ed91e-109">The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="ed91e-110">該命令會將該物件儲存在 $Password 變數中。</span><span class="sxs-lookup"><span data-stu-id="ed91e-110">The command stores that object in the $Password variable.</span></span>

<span data-ttu-id="ed91e-111">第二個命令會修改名為 ContosoCertificate 的憑證。</span><span class="sxs-lookup"><span data-stu-id="ed91e-111">The second command modifies a certificate named ContosoCertificate.</span></span>
<span data-ttu-id="ed91e-112">命令會使用儲存在 $Password 中的密碼。</span><span class="sxs-lookup"><span data-stu-id="ed91e-112">The command uses the password stored in $Password.</span></span>
<span data-ttu-id="ed91e-113">該命令會指定帳戶名稱以及它上傳檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="ed91e-113">The command specifies the account name and the path of the file that it uploads.</span></span>

## <span data-ttu-id="ed91e-114">參數</span><span class="sxs-lookup"><span data-stu-id="ed91e-114">PARAMETERS</span></span>

### <span data-ttu-id="ed91e-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ed91e-115">-AutomationAccountName</span></span>
<span data-ttu-id="ed91e-116">指定此 Cmdlet 修改憑證的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="ed91e-116">Specifies the name of the Automation account for which this cmdlet modifies a certificate.</span></span>

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

### <span data-ttu-id="ed91e-117">-描述</span><span class="sxs-lookup"><span data-stu-id="ed91e-117">-Description</span></span>
<span data-ttu-id="ed91e-118">指定此 Cmdlet 修改之憑證的描述。</span><span class="sxs-lookup"><span data-stu-id="ed91e-118">Specifies a description for the certificate that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="ed91e-119">匯出</span><span class="sxs-lookup"><span data-stu-id="ed91e-119">-Exportable</span></span>
<span data-ttu-id="ed91e-120">指定是否可以匯出證書。</span><span class="sxs-lookup"><span data-stu-id="ed91e-120">Specifies whether the certificate can be exported.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed91e-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="ed91e-121">-Name</span></span>
<span data-ttu-id="ed91e-122">指定此 Cmdlet 所修改之憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="ed91e-122">Specifies the name of the certificate that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="ed91e-123">-Password</span><span class="sxs-lookup"><span data-stu-id="ed91e-123">-Password</span></span>
<span data-ttu-id="ed91e-124">指定憑證檔的密碼。</span><span class="sxs-lookup"><span data-stu-id="ed91e-124">Specifies the password for the certificate file.</span></span>

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

### <span data-ttu-id="ed91e-125">-Path</span><span class="sxs-lookup"><span data-stu-id="ed91e-125">-Path</span></span>
<span data-ttu-id="ed91e-126">指定要上傳的腳本檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="ed91e-126">Specifies the path to a script file to upload.</span></span>
<span data-ttu-id="ed91e-127">檔案可以是 .cer 檔案或 .pfx 檔案。</span><span class="sxs-lookup"><span data-stu-id="ed91e-127">The file can be a .cer file or a .pfx file.</span></span>

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

### <span data-ttu-id="ed91e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed91e-128">-ResourceGroupName</span></span>
<span data-ttu-id="ed91e-129">指定此 Cmdlet 修改憑證之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ed91e-129">Specifies the name of the resource group for which this cmdlet modifies a certificate.</span></span>

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

### <span data-ttu-id="ed91e-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed91e-130">-DefaultProfile</span></span>
<span data-ttu-id="ed91e-131">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ed91e-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed91e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed91e-132">CommonParameters</span></span>
<span data-ttu-id="ed91e-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ed91e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed91e-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ed91e-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed91e-135">輸入</span><span class="sxs-lookup"><span data-stu-id="ed91e-135">INPUTS</span></span>

## <span data-ttu-id="ed91e-136">輸出</span><span class="sxs-lookup"><span data-stu-id="ed91e-136">OUTPUTS</span></span>

### <span data-ttu-id="ed91e-137">CertificateInfo 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ed91e-137">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="ed91e-138">筆記</span><span class="sxs-lookup"><span data-stu-id="ed91e-138">NOTES</span></span>

## <span data-ttu-id="ed91e-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="ed91e-139">RELATED LINKS</span></span>

[<span data-ttu-id="ed91e-140">AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="ed91e-140">Get-AzureRmAutomationCertificate</span></span>](./Get-AzureRMAutomationCertificate.md)

[<span data-ttu-id="ed91e-141">新-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="ed91e-141">New-AzureRmAutomationCertificate</span></span>](./New-AzureRMAutomationCertificate.md)

[<span data-ttu-id="ed91e-142">移除-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="ed91e-142">Remove-AzureRmAutomationCertificate</span></span>](./Remove-AzureRMAutomationCertificate.md)

