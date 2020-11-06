---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: D9CA9515-5C19-4D63-8D4D-0B288E9309E9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/set-azurermintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountCertificate.md
ms.openlocfilehash: 00acd3e13484fe2981d172b4331ff7848c78fc9a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453720"
---
# <span data-ttu-id="9766c-101">Set-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="9766c-101">Set-AzureRmIntegrationAccountCertificate</span></span>

## <span data-ttu-id="9766c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9766c-102">SYNOPSIS</span></span>
<span data-ttu-id="9766c-103">修改整合帳戶憑證。</span><span class="sxs-lookup"><span data-stu-id="9766c-103">Modifies an integration account certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9766c-104">句法</span><span class="sxs-lookup"><span data-stu-id="9766c-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 [-KeyName <String>] [-KeyVersion <String>] [-KeyVaultId <String>] [-PublicCertificateFilePath <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9766c-105">說明</span><span class="sxs-lookup"><span data-stu-id="9766c-105">DESCRIPTION</span></span>
<span data-ttu-id="9766c-106">**AzureRmIntegrationAccountCertificate** Cmdlet 會修改整合帳戶憑證。</span><span class="sxs-lookup"><span data-stu-id="9766c-106">The **Set-AzureRmIntegrationAccountCertificate** cmdlet modifies an integration account certificate.</span></span>
<span data-ttu-id="9766c-107">這個 Cmdlet 會傳回代表整合帳戶憑證的物件。</span><span class="sxs-lookup"><span data-stu-id="9766c-107">This cmdlet returns an object that represents the integration account certificate.</span></span>
<span data-ttu-id="9766c-108">指定整合帳戶名稱、資源群組名稱及憑證名稱。</span><span class="sxs-lookup"><span data-stu-id="9766c-108">Specifying the integration account name, resource group name, and certificate name.</span></span>
<span data-ttu-id="9766c-109">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="9766c-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="9766c-110">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="9766c-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="9766c-111">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="9766c-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="9766c-112">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="9766c-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="9766c-113">示例</span><span class="sxs-lookup"><span data-stu-id="9766c-113">EXAMPLES</span></span>

### <span data-ttu-id="9766c-114">範例1：修改整合帳戶憑證</span><span class="sxs-lookup"><span data-stu-id="9766c-114">Example 1: Modify an integration account certificate</span></span>
```
PS C:\>Set-AzureRmIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegartionAccount31" -CertificateName "IntegrationAccountCertificate01" -KeyName "TestKey" -KeyVersion "1.0" -KeyVaultId "/subscriptions/<subscriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/keyvault" -PublicCertificateFilePath "c:\temp\Certificate.cer"
Id                : /subscriptions/<SusbcriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegartionAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SusbcriptionId/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/testkeyvault
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="9766c-115">這個命令會修改指定資源群組中的整合帳戶憑證。</span><span class="sxs-lookup"><span data-stu-id="9766c-115">This command modifies the integration account certificate in the specified resource group.</span></span>

## <span data-ttu-id="9766c-116">參數</span><span class="sxs-lookup"><span data-stu-id="9766c-116">PARAMETERS</span></span>

### <span data-ttu-id="9766c-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="9766c-117">-CertificateName</span></span>
<span data-ttu-id="9766c-118">指定整合帳戶憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="9766c-118">Specifies the name of an integration account certificate.</span></span>

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

### <span data-ttu-id="9766c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9766c-119">-DefaultProfile</span></span>
<span data-ttu-id="9766c-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="9766c-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9766c-121">-Force</span><span class="sxs-lookup"><span data-stu-id="9766c-121">-Force</span></span>
<span data-ttu-id="9766c-122">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="9766c-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9766c-123">-KeyName</span><span class="sxs-lookup"><span data-stu-id="9766c-123">-KeyName</span></span>
<span data-ttu-id="9766c-124">指定 [主要電子倉庫] 中憑證金鑰的名稱。</span><span class="sxs-lookup"><span data-stu-id="9766c-124">Specifies the name of a certificate key in the key vault.</span></span>

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

### <span data-ttu-id="9766c-125">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="9766c-125">-KeyVaultId</span></span>
<span data-ttu-id="9766c-126">指定金鑰 vault ID。</span><span class="sxs-lookup"><span data-stu-id="9766c-126">Specifies a key vault ID.</span></span>

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

### <span data-ttu-id="9766c-127">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="9766c-127">-KeyVersion</span></span>
<span data-ttu-id="9766c-128">指定 [金鑰 vault] 中的憑證金鑰版本。</span><span class="sxs-lookup"><span data-stu-id="9766c-128">Specifies the version of the certificate key in the key vault.</span></span>

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

### <span data-ttu-id="9766c-129">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="9766c-129">-Metadata</span></span>
<span data-ttu-id="9766c-130">指定憑證的中繼資料物件。</span><span class="sxs-lookup"><span data-stu-id="9766c-130">Specifies a metadata object for the certificate.</span></span>

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

### <span data-ttu-id="9766c-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="9766c-131">-Name</span></span>
<span data-ttu-id="9766c-132">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="9766c-132">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="9766c-133">-PublicCertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="9766c-133">-PublicCertificateFilePath</span></span>
<span data-ttu-id="9766c-134">指定公用憑證 ( .cer) 檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="9766c-134">Specifies the path of a public certificate (.cer) file.</span></span>

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

### <span data-ttu-id="9766c-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9766c-135">-ResourceGroupName</span></span>
<span data-ttu-id="9766c-136">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9766c-136">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="9766c-137">-確認</span><span class="sxs-lookup"><span data-stu-id="9766c-137">-Confirm</span></span>
<span data-ttu-id="9766c-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9766c-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9766c-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9766c-139">-WhatIf</span></span>
<span data-ttu-id="9766c-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9766c-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9766c-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9766c-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9766c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9766c-142">CommonParameters</span></span>
<span data-ttu-id="9766c-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9766c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9766c-144">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9766c-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9766c-145">輸入</span><span class="sxs-lookup"><span data-stu-id="9766c-145">INPUTS</span></span>

### <span data-ttu-id="9766c-146">System.object</span><span class="sxs-lookup"><span data-stu-id="9766c-146">System.String</span></span>

## <span data-ttu-id="9766c-147">輸出</span><span class="sxs-lookup"><span data-stu-id="9766c-147">OUTPUTS</span></span>

### <span data-ttu-id="9766c-148">IntegrationAccountCertificate 的管理邏輯。</span><span class="sxs-lookup"><span data-stu-id="9766c-148">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="9766c-149">筆記</span><span class="sxs-lookup"><span data-stu-id="9766c-149">NOTES</span></span>

## <span data-ttu-id="9766c-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="9766c-150">RELATED LINKS</span></span>

[<span data-ttu-id="9766c-151">AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="9766c-151">Get-AzureRmIntegrationAccountCertificate</span></span>](./Get-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="9766c-152">新-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="9766c-152">New-AzureRmIntegrationAccountCertificate</span></span>](./New-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="9766c-153">移除-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="9766c-153">Remove-AzureRmIntegrationAccountCertificate</span></span>](./Remove-AzureRmIntegrationAccountCertificate.md)


