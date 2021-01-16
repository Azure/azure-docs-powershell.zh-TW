---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: F1A2861F-14EF-4F67-8452-31FD498528BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCertificate.md
ms.openlocfilehash: 7eaaabf374d4ee9b43477596df06f58593c6d1e9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98285195"
---
# <span data-ttu-id="d4e82-101">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="d4e82-101">Set-AzAutomationCertificate</span></span>

## <span data-ttu-id="d4e82-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d4e82-102">SYNOPSIS</span></span>
<span data-ttu-id="d4e82-103">修改自動化憑證的設定。</span><span class="sxs-lookup"><span data-stu-id="d4e82-103">Modifies the configuration of an Automation certificate.</span></span>

## <span data-ttu-id="d4e82-104">句法</span><span class="sxs-lookup"><span data-stu-id="d4e82-104">SYNTAX</span></span>

```
Set-AzAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path <String>] [-Exportable <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4e82-105">說明</span><span class="sxs-lookup"><span data-stu-id="d4e82-105">DESCRIPTION</span></span>
<span data-ttu-id="d4e82-106">AzAutomationCertificate Cmdlet 會修改 Azure 自動化中憑證的 **設定** 。</span><span class="sxs-lookup"><span data-stu-id="d4e82-106">The **Set-AzAutomationCertificate** cmdlet modifies the configuration of a certificate in Azure Automation.</span></span>

## <span data-ttu-id="d4e82-107">示例</span><span class="sxs-lookup"><span data-stu-id="d4e82-107">EXAMPLES</span></span>

### <span data-ttu-id="d4e82-108">範例1：修改憑證</span><span class="sxs-lookup"><span data-stu-id="d4e82-108">Example 1: Modify a certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> Set-AzAutomationCertificate -AutomationAccountName "Contos17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="d4e82-109">使用 ConvertTo-SecureString Cmdlet，第一個命令會將純文字密碼轉換為安全字串。</span><span class="sxs-lookup"><span data-stu-id="d4e82-109">The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="d4e82-110">該命令會將該物件儲存在 $Password 變數中。</span><span class="sxs-lookup"><span data-stu-id="d4e82-110">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="d4e82-111">第二個命令會修改名為 ContosoCertificate 的憑證。</span><span class="sxs-lookup"><span data-stu-id="d4e82-111">The second command modifies a certificate named ContosoCertificate.</span></span>
<span data-ttu-id="d4e82-112">命令會使用儲存在 $Password 中的密碼。</span><span class="sxs-lookup"><span data-stu-id="d4e82-112">The command uses the password stored in $Password.</span></span>
<span data-ttu-id="d4e82-113">該命令會指定帳戶名稱以及它上傳檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="d4e82-113">The command specifies the account name and the path of the file that it uploads.</span></span>

## <span data-ttu-id="d4e82-114">參數</span><span class="sxs-lookup"><span data-stu-id="d4e82-114">PARAMETERS</span></span>

### <span data-ttu-id="d4e82-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d4e82-115">-AutomationAccountName</span></span>
<span data-ttu-id="d4e82-116">指定此 Cmdlet 修改憑證的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="d4e82-116">Specifies the name of the Automation account for which this cmdlet modifies a certificate.</span></span>

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

### <span data-ttu-id="d4e82-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4e82-117">-DefaultProfile</span></span>
<span data-ttu-id="d4e82-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="d4e82-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d4e82-119">-描述</span><span class="sxs-lookup"><span data-stu-id="d4e82-119">-Description</span></span>
<span data-ttu-id="d4e82-120">指定此 Cmdlet 修改之憑證的描述。</span><span class="sxs-lookup"><span data-stu-id="d4e82-120">Specifies a description for the certificate that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="d4e82-121">匯出</span><span class="sxs-lookup"><span data-stu-id="d4e82-121">-Exportable</span></span>
<span data-ttu-id="d4e82-122">指定是否可以匯出證書。</span><span class="sxs-lookup"><span data-stu-id="d4e82-122">Specifies whether the certificate can be exported.</span></span>

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

### <span data-ttu-id="d4e82-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="d4e82-123">-Name</span></span>
<span data-ttu-id="d4e82-124">指定此 Cmdlet 所修改之憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="d4e82-124">Specifies the name of the certificate that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="d4e82-125">-Password</span><span class="sxs-lookup"><span data-stu-id="d4e82-125">-Password</span></span>
<span data-ttu-id="d4e82-126">指定憑證檔的密碼。</span><span class="sxs-lookup"><span data-stu-id="d4e82-126">Specifies the password for the certificate file.</span></span>

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

### <span data-ttu-id="d4e82-127">-Path</span><span class="sxs-lookup"><span data-stu-id="d4e82-127">-Path</span></span>
<span data-ttu-id="d4e82-128">指定要上傳的腳本檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="d4e82-128">Specifies the path to a script file to upload.</span></span>
<span data-ttu-id="d4e82-129">檔案可以是 .cer 檔案或 .pfx 檔案。</span><span class="sxs-lookup"><span data-stu-id="d4e82-129">The file can be a .cer file or a .pfx file.</span></span>

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

### <span data-ttu-id="d4e82-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4e82-130">-ResourceGroupName</span></span>
<span data-ttu-id="d4e82-131">指定此 Cmdlet 修改憑證之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d4e82-131">Specifies the name of the resource group for which this cmdlet modifies a certificate.</span></span>

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

### <span data-ttu-id="d4e82-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4e82-132">CommonParameters</span></span>
<span data-ttu-id="d4e82-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d4e82-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4e82-134">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d4e82-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4e82-135">輸入</span><span class="sxs-lookup"><span data-stu-id="d4e82-135">INPUTS</span></span>

### <span data-ttu-id="d4e82-136">System.object</span><span class="sxs-lookup"><span data-stu-id="d4e82-136">System.String</span></span>

### <span data-ttu-id="d4e82-137">SecureString</span><span class="sxs-lookup"><span data-stu-id="d4e82-137">System.Security.SecureString</span></span>

### <span data-ttu-id="d4e82-138">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中立，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d4e82-138">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="d4e82-139">輸出</span><span class="sxs-lookup"><span data-stu-id="d4e82-139">OUTPUTS</span></span>

### <span data-ttu-id="d4e82-140">CertificateInfo 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d4e82-140">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="d4e82-141">筆記</span><span class="sxs-lookup"><span data-stu-id="d4e82-141">NOTES</span></span>

## <span data-ttu-id="d4e82-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="d4e82-142">RELATED LINKS</span></span>

[<span data-ttu-id="d4e82-143">AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="d4e82-143">Get-AzAutomationCertificate</span></span>](./Get-AzAutomationCertificate.md)

[<span data-ttu-id="d4e82-144">新-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="d4e82-144">New-AzAutomationCertificate</span></span>](./New-AzAutomationCertificate.md)

[<span data-ttu-id="d4e82-145">移除-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="d4e82-145">Remove-AzAutomationCertificate</span></span>](./Remove-AzAutomationCertificate.md)


