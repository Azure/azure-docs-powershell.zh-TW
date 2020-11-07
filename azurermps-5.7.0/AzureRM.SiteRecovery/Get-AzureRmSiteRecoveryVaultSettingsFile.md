---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 9595E785-6DBF-433C-83B3-8506A3B49B13
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVaultSettingsFile.md
ms.openlocfilehash: 621e5ac05c5f975ff3878781bcb8c5a1b40c04bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625417"
---
# <span data-ttu-id="f6ca1-101">Get-AzureRmSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="f6ca1-101">Get-AzureRmSiteRecoveryVaultSettingsFile</span></span>

## <span data-ttu-id="f6ca1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f6ca1-102">SYNOPSIS</span></span>
<span data-ttu-id="f6ca1-103">取得網站復原電子倉庫設定檔案。</span><span class="sxs-lookup"><span data-stu-id="f6ca1-103">Gets the Site Recovery vault settings file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6ca1-104">句法</span><span class="sxs-lookup"><span data-stu-id="f6ca1-104">SYNTAX</span></span>

### <span data-ttu-id="f6ca1-105">ByParam (預設) </span><span class="sxs-lookup"><span data-stu-id="f6ca1-105">ByParam (Default)</span></span>
```
Get-AzureRmSiteRecoveryVaultSettingsFile [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6ca1-106">設置</span><span class="sxs-lookup"><span data-stu-id="f6ca1-106">Default</span></span>
```
Get-AzureRmSiteRecoveryVaultSettingsFile -Vault <ASRVault> [-Path <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6ca1-107">ForSite</span><span class="sxs-lookup"><span data-stu-id="f6ca1-107">ForSite</span></span>
```
Get-AzureRmSiteRecoveryVaultSettingsFile -Vault <ASRVault> -SiteIdentifier <String> -SiteFriendlyName <String>
 [-Path <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6ca1-108">說明</span><span class="sxs-lookup"><span data-stu-id="f6ca1-108">DESCRIPTION</span></span>
<span data-ttu-id="f6ca1-109">**AzureRmSiteRecoveryVaultSettingsFile** Cmdlet 會取得 Azure Site Recovery 保存庫的設定檔案。</span><span class="sxs-lookup"><span data-stu-id="f6ca1-109">The **Get-AzureRmSiteRecoveryVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="f6ca1-110">示例</span><span class="sxs-lookup"><span data-stu-id="f6ca1-110">EXAMPLES</span></span>

## <span data-ttu-id="f6ca1-111">參數</span><span class="sxs-lookup"><span data-stu-id="f6ca1-111">PARAMETERS</span></span>

### <span data-ttu-id="f6ca1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6ca1-112">-DefaultProfile</span></span>
<span data-ttu-id="f6ca1-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f6ca1-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6ca1-114">-Path</span><span class="sxs-lookup"><span data-stu-id="f6ca1-114">-Path</span></span>
<span data-ttu-id="f6ca1-115">指定網站復原電子倉庫設定檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="f6ca1-115">Specifies the path to the Site Recovery vault settings file.</span></span>
<span data-ttu-id="f6ca1-116">若要在本機儲存此檔案，請在命令完成後從網站復原電子倉庫入口網站下載。</span><span class="sxs-lookup"><span data-stu-id="f6ca1-116">To store this file locally, download it from the Site Recovery vault portal once the command completes.</span></span>

```yaml
Type: String
Parameter Sets: Default, ForSite
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6ca1-117">-SiteFriendlyName</span><span class="sxs-lookup"><span data-stu-id="f6ca1-117">-SiteFriendlyName</span></span>
<span data-ttu-id="f6ca1-118">當網站為 Hyper-v 網站時，指定電子倉庫的網站易記名稱。</span><span class="sxs-lookup"><span data-stu-id="f6ca1-118">Specifies the site friendly name for the vault when the site is a Hyper-V site.</span></span>

```yaml
Type: String
Parameter Sets: ForSite
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6ca1-119">-SiteIdentifier</span><span class="sxs-lookup"><span data-stu-id="f6ca1-119">-SiteIdentifier</span></span>
<span data-ttu-id="f6ca1-120">指定當網站為 Hyper-v 網站時，保存庫的網站識別碼。</span><span class="sxs-lookup"><span data-stu-id="f6ca1-120">Specifies the site identifier for the vault when the site is a Hyper-V site.</span></span>

```yaml
Type: String
Parameter Sets: ForSite
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6ca1-121">-保存庫</span><span class="sxs-lookup"><span data-stu-id="f6ca1-121">-Vault</span></span>
<span data-ttu-id="f6ca1-122">指定網站的 vault 物件。</span><span class="sxs-lookup"><span data-stu-id="f6ca1-122">Specifies the vault object for the site.</span></span>

```yaml
Type: ASRVault
Parameter Sets: Default, ForSite
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6ca1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6ca1-123">CommonParameters</span></span>
<span data-ttu-id="f6ca1-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f6ca1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6ca1-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f6ca1-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6ca1-126">輸入</span><span class="sxs-lookup"><span data-stu-id="f6ca1-126">INPUTS</span></span>

### <span data-ttu-id="f6ca1-127">ASRVault</span><span class="sxs-lookup"><span data-stu-id="f6ca1-127">ASRVault</span></span>
<span data-ttu-id="f6ca1-128">參數 "Vault" 接受來自管線的 "ASRVault" 類型值</span><span class="sxs-lookup"><span data-stu-id="f6ca1-128">Parameter 'Vault' accepts value of type 'ASRVault' from the pipeline</span></span>

## <span data-ttu-id="f6ca1-129">輸出</span><span class="sxs-lookup"><span data-stu-id="f6ca1-129">OUTPUTS</span></span>

### <span data-ttu-id="f6ca1-130">VaultSettingsFilePath 中的 SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="f6ca1-130">Microsoft.Azure.Commands.SiteRecovery.VaultSettingsFilePath</span></span>

## <span data-ttu-id="f6ca1-131">筆記</span><span class="sxs-lookup"><span data-stu-id="f6ca1-131">NOTES</span></span>

## <span data-ttu-id="f6ca1-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="f6ca1-132">RELATED LINKS</span></span>

[<span data-ttu-id="f6ca1-133">匯入-AzureRmSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="f6ca1-133">Import-AzureRmSiteRecoveryVaultSettingsFile</span></span>](./Import-AzureRmSiteRecoveryVaultSettingsFile.md)

[<span data-ttu-id="f6ca1-134">Set-AzureRmSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="f6ca1-134">Set-AzureRmSiteRecoveryVaultSettings</span></span>](./Set-AzureRmSiteRecoveryVaultSettings.md)
