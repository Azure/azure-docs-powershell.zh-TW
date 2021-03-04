---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/import-AzWebAppKeyVaultCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Import-AzWebAppKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Import-AzWebAppKeyVaultCertificate.md
ms.openlocfilehash: d92aa19573a238d7f54a21f7888bbd93ac07107b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916309"
---
# <span data-ttu-id="78443-101">Import-AzWebAppKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="78443-101">Import-AzWebAppKeyVaultCertificate</span></span>

## <span data-ttu-id="78443-102">簡介</span><span class="sxs-lookup"><span data-stu-id="78443-102">SYNOPSIS</span></span>
<span data-ttu-id="78443-103">從 Key Vault 將 SSL 憑證匯出至 Web App。</span><span class="sxs-lookup"><span data-stu-id="78443-103">Import an SSL certificate to a web app from Key Vault.</span></span>

## <span data-ttu-id="78443-104">語法</span><span class="sxs-lookup"><span data-stu-id="78443-104">SYNTAX</span></span>

```
Import-AzWebAppKeyVaultCertificate [-KeyVaultName] <String> [-CertName] <String> [-ResourceGroupName] <String>
 [-WebAppName] <String> [-Slot <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="78443-105">描述</span><span class="sxs-lookup"><span data-stu-id="78443-105">DESCRIPTION</span></span>
<span data-ttu-id="78443-106">**Import-AzWebAppKeyVaultCertificate** Cmdlet 會從 Key Vault 將 SSL 憑證導入至 Web App。</span><span class="sxs-lookup"><span data-stu-id="78443-106">The **Import-AzWebAppKeyVaultCertificate** cmdlet imports an SSL certificate to a web app from Key Vault.</span></span>

## <span data-ttu-id="78443-107">例子</span><span class="sxs-lookup"><span data-stu-id="78443-107">EXAMPLES</span></span>

### <span data-ttu-id="78443-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="78443-108">Example 1</span></span>
```powershell
PS C:\> Import-AzWebAppKeyVaultCertificate -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" 
-KeyVaultName "ContosoKeyVault" -CertName "ContosoCertname"
```

<span data-ttu-id="78443-109">此命令會從 Key Vault 將 SSL 憑證導入至 Web App。</span><span class="sxs-lookup"><span data-stu-id="78443-109">This command imports an SSL certificate to a web app from Key Vault.</span></span>

### <span data-ttu-id="78443-110">範例 2</span><span class="sxs-lookup"><span data-stu-id="78443-110">Example 2</span></span>
```powershell
PS C:\> Import-AzWebAppKeyVaultCertificate -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" 
-KeyVaultName  '/subscriptions/[sub id]/resourceGroups/[rg]/providers/Microsoft.KeyVault/vaults/[vault name]' 
-CertName "ContosoCertname"
```

<span data-ttu-id="78443-111">此命令會使用資源識別碼將 SSL 憑證從 Key Vault (到 Web App，通常是在金鑰庫位於另一個訂閱中時) 。</span><span class="sxs-lookup"><span data-stu-id="78443-111">This command Import an SSL certificate to a web app from Key Vault using resource id (typically if Key Vault is in another subscription).</span></span>

## <span data-ttu-id="78443-112">參數</span><span class="sxs-lookup"><span data-stu-id="78443-112">PARAMETERS</span></span>

### <span data-ttu-id="78443-113">-CertName</span><span class="sxs-lookup"><span data-stu-id="78443-113">-CertName</span></span>
<span data-ttu-id="78443-114">在 keyvault 中建立之憑證的 KeyVaultCertName</span><span class="sxs-lookup"><span data-stu-id="78443-114">KeyVaultCertName of the certificate created in keyvault</span></span>

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

### <span data-ttu-id="78443-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78443-115">-DefaultProfile</span></span>
<span data-ttu-id="78443-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="78443-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78443-117">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="78443-117">-KeyVaultName</span></span>
<span data-ttu-id="78443-118">Keyvault 的名稱。</span><span class="sxs-lookup"><span data-stu-id="78443-118">The name of the keyvault.</span></span>

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

### <span data-ttu-id="78443-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78443-119">-ResourceGroupName</span></span>
<span data-ttu-id="78443-120">Webapp 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="78443-120">The name of the webapp resource group.</span></span>

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

### <span data-ttu-id="78443-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="78443-121">-Slot</span></span>
<span data-ttu-id="78443-122">Webapp 插槽的名稱。</span><span class="sxs-lookup"><span data-stu-id="78443-122">The name of the webapp slot.</span></span>

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

### <span data-ttu-id="78443-123">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="78443-123">-WebAppName</span></span>
<span data-ttu-id="78443-124">網頁應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="78443-124">The name of the webapp.</span></span>

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

### <span data-ttu-id="78443-125">-確認</span><span class="sxs-lookup"><span data-stu-id="78443-125">-Confirm</span></span>
<span data-ttu-id="78443-126">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="78443-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78443-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78443-127">-WhatIf</span></span>
<span data-ttu-id="78443-128">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="78443-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78443-129">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="78443-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78443-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78443-130">CommonParameters</span></span>
<span data-ttu-id="78443-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="78443-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78443-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="78443-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78443-133">輸入</span><span class="sxs-lookup"><span data-stu-id="78443-133">INPUTS</span></span>

### <span data-ttu-id="78443-134">沒有</span><span class="sxs-lookup"><span data-stu-id="78443-134">None</span></span>

## <span data-ttu-id="78443-135">輸出</span><span class="sxs-lookup"><span data-stu-id="78443-135">OUTPUTS</span></span>

### <span data-ttu-id="78443-136">Microsoft.Azure.Commands.WebApps.models.WebApp.PSCertificate</span><span class="sxs-lookup"><span data-stu-id="78443-136">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSCertificate</span></span>

## <span data-ttu-id="78443-137">筆記</span><span class="sxs-lookup"><span data-stu-id="78443-137">NOTES</span></span>

## <span data-ttu-id="78443-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="78443-138">RELATED LINKS</span></span>
