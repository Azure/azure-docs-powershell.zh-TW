---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: F1A2861F-14EF-4F67-8452-31FD498528BB
online version: https://docs.microsoft.com/powershell/module/az.automation/set-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCertificate.md
ms.openlocfilehash: 80a33fe4664e4c7814db6774e7cd427dd9a2c87e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903354"
---
# <span data-ttu-id="1cfc3-101">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="1cfc3-101">Set-AzAutomationCertificate</span></span>

## <span data-ttu-id="1cfc3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1cfc3-102">SYNOPSIS</span></span>
<span data-ttu-id="1cfc3-103">修改自動化憑證的群組原則。</span><span class="sxs-lookup"><span data-stu-id="1cfc3-103">Modifies the configuration of an Automation certificate.</span></span>

## <span data-ttu-id="1cfc3-104">語法</span><span class="sxs-lookup"><span data-stu-id="1cfc3-104">SYNTAX</span></span>

```
Set-AzAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path <String>] [-Exportable <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1cfc3-105">描述</span><span class="sxs-lookup"><span data-stu-id="1cfc3-105">DESCRIPTION</span></span>
<span data-ttu-id="1cfc3-106">**Set-AzAutomationCertificate** Cmdlet 會修改 Azure Automation 中憑證的設定。</span><span class="sxs-lookup"><span data-stu-id="1cfc3-106">The **Set-AzAutomationCertificate** cmdlet modifies the configuration of a certificate in Azure Automation.</span></span>

## <span data-ttu-id="1cfc3-107">例子</span><span class="sxs-lookup"><span data-stu-id="1cfc3-107">EXAMPLES</span></span>

### <span data-ttu-id="1cfc3-108">範例 1：修改憑證</span><span class="sxs-lookup"><span data-stu-id="1cfc3-108">Example 1: Modify a certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> Set-AzAutomationCertificate -AutomationAccountName "Contos17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="1cfc3-109">第一個命令會使用 Cmdlet 將純文字密碼轉換為ConvertTo-SecureString字串。</span><span class="sxs-lookup"><span data-stu-id="1cfc3-109">The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="1cfc3-110">該命令將該物件儲存在$Password變數中。</span><span class="sxs-lookup"><span data-stu-id="1cfc3-110">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="1cfc3-111">第二個命令會修改名為 ContosoCertificate 的憑證。</span><span class="sxs-lookup"><span data-stu-id="1cfc3-111">The second command modifies a certificate named ContosoCertificate.</span></span>
<span data-ttu-id="1cfc3-112">命令使用儲存在 $Password。</span><span class="sxs-lookup"><span data-stu-id="1cfc3-112">The command uses the password stored in $Password.</span></span>
<span data-ttu-id="1cfc3-113">命令會指定帳戶名稱及其上傳之檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="1cfc3-113">The command specifies the account name and the path of the file that it uploads.</span></span>

## <span data-ttu-id="1cfc3-114">參數</span><span class="sxs-lookup"><span data-stu-id="1cfc3-114">PARAMETERS</span></span>

### <span data-ttu-id="1cfc3-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1cfc3-115">-AutomationAccountName</span></span>
<span data-ttu-id="1cfc3-116">指定此 Cmdlet 修改憑證的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="1cfc3-116">Specifies the name of the Automation account for which this cmdlet modifies a certificate.</span></span>

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

### <span data-ttu-id="1cfc3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cfc3-117">-DefaultProfile</span></span>
<span data-ttu-id="1cfc3-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="1cfc3-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1cfc3-119">-描述</span><span class="sxs-lookup"><span data-stu-id="1cfc3-119">-Description</span></span>
<span data-ttu-id="1cfc3-120">指定此 Cmdlet 修改之憑證的描述。</span><span class="sxs-lookup"><span data-stu-id="1cfc3-120">Specifies a description for the certificate that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="1cfc3-121">-可匯出</span><span class="sxs-lookup"><span data-stu-id="1cfc3-121">-Exportable</span></span>
<span data-ttu-id="1cfc3-122">指定是否可以匯出憑證。</span><span class="sxs-lookup"><span data-stu-id="1cfc3-122">Specifies whether the certificate can be exported.</span></span>

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

### <span data-ttu-id="1cfc3-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="1cfc3-123">-Name</span></span>
<span data-ttu-id="1cfc3-124">指定此 Cmdlet 修改的憑證名稱。</span><span class="sxs-lookup"><span data-stu-id="1cfc3-124">Specifies the name of the certificate that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="1cfc3-125">-密碼</span><span class="sxs-lookup"><span data-stu-id="1cfc3-125">-Password</span></span>
<span data-ttu-id="1cfc3-126">指定憑證檔案的密碼。</span><span class="sxs-lookup"><span data-stu-id="1cfc3-126">Specifies the password for the certificate file.</span></span>

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

### <span data-ttu-id="1cfc3-127">-路徑</span><span class="sxs-lookup"><span data-stu-id="1cfc3-127">-Path</span></span>
<span data-ttu-id="1cfc3-128">指定要上傳腳本檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="1cfc3-128">Specifies the path to a script file to upload.</span></span>
<span data-ttu-id="1cfc3-129">檔案可以是 .cer 檔案或 .pfx 檔案。</span><span class="sxs-lookup"><span data-stu-id="1cfc3-129">The file can be a .cer file or a .pfx file.</span></span>

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

### <span data-ttu-id="1cfc3-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cfc3-130">-ResourceGroupName</span></span>
<span data-ttu-id="1cfc3-131">指定此 Cmdlet 修改憑證的資源組名。</span><span class="sxs-lookup"><span data-stu-id="1cfc3-131">Specifies the name of the resource group for which this cmdlet modifies a certificate.</span></span>

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

### <span data-ttu-id="1cfc3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cfc3-132">CommonParameters</span></span>
<span data-ttu-id="1cfc3-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1cfc3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cfc3-134">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="1cfc3-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cfc3-135">輸入</span><span class="sxs-lookup"><span data-stu-id="1cfc3-135">INPUTS</span></span>

### <span data-ttu-id="1cfc3-136">System.String</span><span class="sxs-lookup"><span data-stu-id="1cfc3-136">System.String</span></span>

### <span data-ttu-id="1cfc3-137">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="1cfc3-137">System.Security.SecureString</span></span>

### <span data-ttu-id="1cfc3-138">System.Nullable'1[[System.Boolean， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1cfc3-138">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="1cfc3-139">輸出</span><span class="sxs-lookup"><span data-stu-id="1cfc3-139">OUTPUTS</span></span>

### <span data-ttu-id="1cfc3-140">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="1cfc3-140">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="1cfc3-141">筆記</span><span class="sxs-lookup"><span data-stu-id="1cfc3-141">NOTES</span></span>

## <span data-ttu-id="1cfc3-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="1cfc3-142">RELATED LINKS</span></span>

[<span data-ttu-id="1cfc3-143">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="1cfc3-143">Get-AzAutomationCertificate</span></span>](./Get-AzAutomationCertificate.md)

[<span data-ttu-id="1cfc3-144">New-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="1cfc3-144">New-AzAutomationCertificate</span></span>](./New-AzAutomationCertificate.md)

[<span data-ttu-id="1cfc3-145">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="1cfc3-145">Remove-AzAutomationCertificate</span></span>](./Remove-AzAutomationCertificate.md)


