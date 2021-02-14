---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/import-AzWebAppKeyVaultCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Import-AzWebAppKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Import-AzWebAppKeyVaultCertificate.md
ms.openlocfilehash: 61f498a521134ee0abb74f45ff048c94e7c53081
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100134267"
---
# <span data-ttu-id="e62a2-101">Import-AzWebAppKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="e62a2-101">Import-AzWebAppKeyVaultCertificate</span></span>

## <span data-ttu-id="e62a2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e62a2-102">SYNOPSIS</span></span>
<span data-ttu-id="e62a2-103">從主要電子倉庫將 SSL 憑證匯入至 web 應用程式。</span><span class="sxs-lookup"><span data-stu-id="e62a2-103">Import an SSL certificate to a web app from Key Vault.</span></span>

## <span data-ttu-id="e62a2-104">句法</span><span class="sxs-lookup"><span data-stu-id="e62a2-104">SYNTAX</span></span>

```
Import-AzWebAppKeyVaultCertificate [-KeyVaultName] <String> [-CertName] <String> [-ResourceGroupName] <String>
 [-WebAppName] <String> [-Slot <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e62a2-105">說明</span><span class="sxs-lookup"><span data-stu-id="e62a2-105">DESCRIPTION</span></span>
<span data-ttu-id="e62a2-106">匯 **入-AzWebAppKeyVaultCertificate** Cmdlet 會從主要電子倉庫將 SSL 憑證匯入至 web app。</span><span class="sxs-lookup"><span data-stu-id="e62a2-106">The **Import-AzWebAppKeyVaultCertificate** cmdlet imports an SSL certificate to a web app from Key Vault.</span></span>

## <span data-ttu-id="e62a2-107">示例</span><span class="sxs-lookup"><span data-stu-id="e62a2-107">EXAMPLES</span></span>

### <span data-ttu-id="e62a2-108">範例1</span><span class="sxs-lookup"><span data-stu-id="e62a2-108">Example 1</span></span>
```powershell
PS C:\> Import-AzWebAppKeyVaultCertificate -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" 
-KeyVaultName "ContosoKeyVault" -CertName "ContosoCertname"
```

<span data-ttu-id="e62a2-109">這個命令會從主要電子倉庫將 SSL 憑證從 web app 匯入。</span><span class="sxs-lookup"><span data-stu-id="e62a2-109">This command imports an SSL certificate to a web app from Key Vault.</span></span>

### <span data-ttu-id="e62a2-110">範例2</span><span class="sxs-lookup"><span data-stu-id="e62a2-110">Example 2</span></span>
```powershell
PS C:\> Import-AzWebAppKeyVaultCertificate -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" 
-KeyVaultName  '/subscriptions/[sub id]/resourceGroups/[rg]/providers/Microsoft.KeyVault/vaults/[vault name]' 
-CertName "ContosoCertname"
```

<span data-ttu-id="e62a2-111">這個命令會使用資源識別碼從主要電子倉庫將 SSL 憑證匯入至 web app， (通常是在另一個訂閱) 中。</span><span class="sxs-lookup"><span data-stu-id="e62a2-111">This command Import an SSL certificate to a web app from Key Vault using resource id (typically if Key Vault is in another subscription).</span></span>

## <span data-ttu-id="e62a2-112">參數</span><span class="sxs-lookup"><span data-stu-id="e62a2-112">PARAMETERS</span></span>

### <span data-ttu-id="e62a2-113">-CertName</span><span class="sxs-lookup"><span data-stu-id="e62a2-113">-CertName</span></span>
<span data-ttu-id="e62a2-114">在 keyvault 中建立的憑證 KeyVaultCertName</span><span class="sxs-lookup"><span data-stu-id="e62a2-114">KeyVaultCertName of the certificate created in keyvault</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e62a2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e62a2-115">-DefaultProfile</span></span>
<span data-ttu-id="e62a2-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e62a2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e62a2-117">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="e62a2-117">-KeyVaultName</span></span>
<span data-ttu-id="e62a2-118">Keyvault 的名稱。</span><span class="sxs-lookup"><span data-stu-id="e62a2-118">The name of the keyvault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e62a2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e62a2-119">-ResourceGroupName</span></span>
<span data-ttu-id="e62a2-120">Webapp 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e62a2-120">The name of the webapp resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e62a2-121">-槽</span><span class="sxs-lookup"><span data-stu-id="e62a2-121">-Slot</span></span>
<span data-ttu-id="e62a2-122">Webapp 槽的名稱。</span><span class="sxs-lookup"><span data-stu-id="e62a2-122">The name of the webapp slot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e62a2-123">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="e62a2-123">-WebAppName</span></span>
<span data-ttu-id="e62a2-124">Webapp 的名稱。</span><span class="sxs-lookup"><span data-stu-id="e62a2-124">The name of the webapp.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e62a2-125">-確認</span><span class="sxs-lookup"><span data-stu-id="e62a2-125">-Confirm</span></span>
<span data-ttu-id="e62a2-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e62a2-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e62a2-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e62a2-127">-WhatIf</span></span>
<span data-ttu-id="e62a2-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e62a2-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e62a2-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e62a2-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e62a2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e62a2-130">CommonParameters</span></span>
<span data-ttu-id="e62a2-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e62a2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e62a2-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e62a2-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e62a2-133">輸入</span><span class="sxs-lookup"><span data-stu-id="e62a2-133">INPUTS</span></span>

### <span data-ttu-id="e62a2-134">所有</span><span class="sxs-lookup"><span data-stu-id="e62a2-134">None</span></span>

## <span data-ttu-id="e62a2-135">輸出</span><span class="sxs-lookup"><span data-stu-id="e62a2-135">OUTPUTS</span></span>

### <span data-ttu-id="e62a2-136">WebApps WebApp. PSCertificate （）</span><span class="sxs-lookup"><span data-stu-id="e62a2-136">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSCertificate</span></span>

## <span data-ttu-id="e62a2-137">筆記</span><span class="sxs-lookup"><span data-stu-id="e62a2-137">NOTES</span></span>

## <span data-ttu-id="e62a2-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="e62a2-138">RELATED LINKS</span></span>
