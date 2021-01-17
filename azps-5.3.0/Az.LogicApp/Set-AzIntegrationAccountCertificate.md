---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: D9CA9515-5C19-4D63-8D4D-0B288E9309E9
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountCertificate.md
ms.openlocfilehash: 5b8da61caf8e3a89572f2054aea101a1ad8b70c6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434940"
---
# <span data-ttu-id="e5355-101">Set-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="e5355-101">Set-AzIntegrationAccountCertificate</span></span>

## <span data-ttu-id="e5355-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e5355-102">SYNOPSIS</span></span>
<span data-ttu-id="e5355-103">修改整合帳戶憑證。</span><span class="sxs-lookup"><span data-stu-id="e5355-103">Modifies an integration account certificate.</span></span>

## <span data-ttu-id="e5355-104">句法</span><span class="sxs-lookup"><span data-stu-id="e5355-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 [-KeyName <String>] [-KeyVersion <String>] [-KeyVaultId <String>] [-PublicCertificateFilePath <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e5355-105">說明</span><span class="sxs-lookup"><span data-stu-id="e5355-105">DESCRIPTION</span></span>
<span data-ttu-id="e5355-106">**AzIntegrationAccountCertificate** Cmdlet 會修改整合帳戶憑證。</span><span class="sxs-lookup"><span data-stu-id="e5355-106">The **Set-AzIntegrationAccountCertificate** cmdlet modifies an integration account certificate.</span></span>
<span data-ttu-id="e5355-107">這個 Cmdlet 會傳回代表整合帳戶憑證的物件。</span><span class="sxs-lookup"><span data-stu-id="e5355-107">This cmdlet returns an object that represents the integration account certificate.</span></span>
<span data-ttu-id="e5355-108">指定整合帳戶名稱、資源群組名稱及憑證名稱。</span><span class="sxs-lookup"><span data-stu-id="e5355-108">Specifying the integration account name, resource group name, and certificate name.</span></span>
<span data-ttu-id="e5355-109">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="e5355-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="e5355-110">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="e5355-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="e5355-111">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="e5355-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="e5355-112">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="e5355-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="e5355-113">示例</span><span class="sxs-lookup"><span data-stu-id="e5355-113">EXAMPLES</span></span>

### <span data-ttu-id="e5355-114">範例1：修改整合帳戶憑證</span><span class="sxs-lookup"><span data-stu-id="e5355-114">Example 1: Modify an integration account certificate</span></span>
```
PS C:\>Set-AzIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01" -KeyName "TestKey" -KeyVersion "1.0" -KeyVaultId "/subscriptions/<subscriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/keyvault" -PublicCertificateFilePath "c:\temp\Certificate.cer"
Id                : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SubscriptionId/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/testkeyvault
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="e5355-115">這個命令會修改指定資源群組中的整合帳戶憑證。</span><span class="sxs-lookup"><span data-stu-id="e5355-115">This command modifies the integration account certificate in the specified resource group.</span></span>

## <span data-ttu-id="e5355-116">參數</span><span class="sxs-lookup"><span data-stu-id="e5355-116">PARAMETERS</span></span>

### <span data-ttu-id="e5355-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="e5355-117">-CertificateName</span></span>
<span data-ttu-id="e5355-118">指定整合帳戶憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="e5355-118">Specifies the name of an integration account certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5355-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5355-119">-DefaultProfile</span></span>
<span data-ttu-id="e5355-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e5355-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e5355-121">-Force</span><span class="sxs-lookup"><span data-stu-id="e5355-121">-Force</span></span>
<span data-ttu-id="e5355-122">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="e5355-122">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5355-123">-KeyName</span><span class="sxs-lookup"><span data-stu-id="e5355-123">-KeyName</span></span>
<span data-ttu-id="e5355-124">指定 [主要電子倉庫] 中憑證金鑰的名稱。</span><span class="sxs-lookup"><span data-stu-id="e5355-124">Specifies the name of a certificate key in the key vault.</span></span>

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

### <span data-ttu-id="e5355-125">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="e5355-125">-KeyVaultId</span></span>
<span data-ttu-id="e5355-126">指定金鑰 vault ID。</span><span class="sxs-lookup"><span data-stu-id="e5355-126">Specifies a key vault ID.</span></span>

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

### <span data-ttu-id="e5355-127">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="e5355-127">-KeyVersion</span></span>
<span data-ttu-id="e5355-128">指定 [金鑰 vault] 中的憑證金鑰版本。</span><span class="sxs-lookup"><span data-stu-id="e5355-128">Specifies the version of the certificate key in the key vault.</span></span>

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

### <span data-ttu-id="e5355-129">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="e5355-129">-Metadata</span></span>
<span data-ttu-id="e5355-130">指定憑證的中繼資料物件。</span><span class="sxs-lookup"><span data-stu-id="e5355-130">Specifies a metadata object for the certificate.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5355-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="e5355-131">-Name</span></span>
<span data-ttu-id="e5355-132">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="e5355-132">Specifies the name of the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5355-133">-PublicCertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="e5355-133">-PublicCertificateFilePath</span></span>
<span data-ttu-id="e5355-134">指定公用憑證 ( .cer) 檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="e5355-134">Specifies the path of a public certificate (.cer) file.</span></span>

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

### <span data-ttu-id="e5355-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5355-135">-ResourceGroupName</span></span>
<span data-ttu-id="e5355-136">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e5355-136">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5355-137">-確認</span><span class="sxs-lookup"><span data-stu-id="e5355-137">-Confirm</span></span>
<span data-ttu-id="e5355-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e5355-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5355-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5355-139">-WhatIf</span></span>
<span data-ttu-id="e5355-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e5355-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5355-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5355-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5355-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5355-142">CommonParameters</span></span>
<span data-ttu-id="e5355-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e5355-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5355-144">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e5355-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5355-145">輸入</span><span class="sxs-lookup"><span data-stu-id="e5355-145">INPUTS</span></span>

### <span data-ttu-id="e5355-146">System.object</span><span class="sxs-lookup"><span data-stu-id="e5355-146">System.String</span></span>

## <span data-ttu-id="e5355-147">輸出</span><span class="sxs-lookup"><span data-stu-id="e5355-147">OUTPUTS</span></span>

### <span data-ttu-id="e5355-148">IntegrationAccountCertificate 的管理邏輯。</span><span class="sxs-lookup"><span data-stu-id="e5355-148">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="e5355-149">筆記</span><span class="sxs-lookup"><span data-stu-id="e5355-149">NOTES</span></span>

## <span data-ttu-id="e5355-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="e5355-150">RELATED LINKS</span></span>

[<span data-ttu-id="e5355-151">AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="e5355-151">Get-AzIntegrationAccountCertificate</span></span>](./Get-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="e5355-152">新-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="e5355-152">New-AzIntegrationAccountCertificate</span></span>](./New-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="e5355-153">移除-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="e5355-153">Remove-AzIntegrationAccountCertificate</span></span>](./Remove-AzIntegrationAccountCertificate.md)


