---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 9595E785-6DBF-433C-83B3-8506A3B49B13
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVaultSettingsFile.md
ms.openlocfilehash: 242dfd46b179d1e7d55613d938eddf5b691da6c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625959"
---
# <span data-ttu-id="0c478-101">Get-AzureRmSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="0c478-101">Get-AzureRmSiteRecoveryVaultSettingsFile</span></span>

## <span data-ttu-id="0c478-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0c478-102">SYNOPSIS</span></span>
<span data-ttu-id="0c478-103">取得網站復原電子倉庫設定檔案。</span><span class="sxs-lookup"><span data-stu-id="0c478-103">Gets the Site Recovery vault settings file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c478-104">句法</span><span class="sxs-lookup"><span data-stu-id="0c478-104">SYNTAX</span></span>

### <span data-ttu-id="0c478-105">ByParam (預設) </span><span class="sxs-lookup"><span data-stu-id="0c478-105">ByParam (Default)</span></span>
```
Get-AzureRmSiteRecoveryVaultSettingsFile [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c478-106">設置</span><span class="sxs-lookup"><span data-stu-id="0c478-106">Default</span></span>
```
Get-AzureRmSiteRecoveryVaultSettingsFile -Vault <ASRVault> [-Path <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c478-107">ForSite</span><span class="sxs-lookup"><span data-stu-id="0c478-107">ForSite</span></span>
```
Get-AzureRmSiteRecoveryVaultSettingsFile -Vault <ASRVault> -SiteIdentifier <String> -SiteFriendlyName <String>
 [-Path <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c478-108">說明</span><span class="sxs-lookup"><span data-stu-id="0c478-108">DESCRIPTION</span></span>
<span data-ttu-id="0c478-109">**AzureRmSiteRecoveryVaultSettingsFile** Cmdlet 會取得 Azure Site Recovery 保存庫的設定檔案。</span><span class="sxs-lookup"><span data-stu-id="0c478-109">The **Get-AzureRmSiteRecoveryVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="0c478-110">示例</span><span class="sxs-lookup"><span data-stu-id="0c478-110">EXAMPLES</span></span>

## <span data-ttu-id="0c478-111">參數</span><span class="sxs-lookup"><span data-stu-id="0c478-111">PARAMETERS</span></span>

### <span data-ttu-id="0c478-112">-Path</span><span class="sxs-lookup"><span data-stu-id="0c478-112">-Path</span></span>
<span data-ttu-id="0c478-113">指定網站復原電子倉庫設定檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="0c478-113">Specifies the path to the Site Recovery vault settings file.</span></span>
<span data-ttu-id="0c478-114">若要在本機儲存此檔案，請在命令完成後從網站復原電子倉庫入口網站下載。</span><span class="sxs-lookup"><span data-stu-id="0c478-114">To store this file locally, download it from the Site Recovery vault portal once the command completes.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, ForSite
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c478-115">-SiteFriendlyName</span><span class="sxs-lookup"><span data-stu-id="0c478-115">-SiteFriendlyName</span></span>
<span data-ttu-id="0c478-116">當網站為 Hyper-v 網站時，指定電子倉庫的網站易記名稱。</span><span class="sxs-lookup"><span data-stu-id="0c478-116">Specifies the site friendly name for the vault when the site is a Hyper-V site.</span></span>

```yaml
Type: System.String
Parameter Sets: ForSite
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c478-117">-SiteIdentifier</span><span class="sxs-lookup"><span data-stu-id="0c478-117">-SiteIdentifier</span></span>
<span data-ttu-id="0c478-118">指定當網站為 Hyper-v 網站時，保存庫的網站識別碼。</span><span class="sxs-lookup"><span data-stu-id="0c478-118">Specifies the site identifier for the vault when the site is a Hyper-V site.</span></span>

```yaml
Type: System.String
Parameter Sets: ForSite
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c478-119">-保存庫</span><span class="sxs-lookup"><span data-stu-id="0c478-119">-Vault</span></span>
<span data-ttu-id="0c478-120">指定網站的 vault 物件。</span><span class="sxs-lookup"><span data-stu-id="0c478-120">Specifies the vault object for the site.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRVault
Parameter Sets: Default, ForSite
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0c478-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c478-121">-DefaultProfile</span></span>
<span data-ttu-id="0c478-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0c478-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c478-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c478-123">CommonParameters</span></span>
<span data-ttu-id="0c478-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0c478-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c478-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0c478-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c478-126">輸入</span><span class="sxs-lookup"><span data-stu-id="0c478-126">INPUTS</span></span>

### <span data-ttu-id="0c478-127">ASRVault</span><span class="sxs-lookup"><span data-stu-id="0c478-127">ASRVault</span></span>
<span data-ttu-id="0c478-128">參數 "Vault" 接受來自管線的 "ASRVault" 類型值</span><span class="sxs-lookup"><span data-stu-id="0c478-128">Parameter 'Vault' accepts value of type 'ASRVault' from the pipeline</span></span>

## <span data-ttu-id="0c478-129">輸出</span><span class="sxs-lookup"><span data-stu-id="0c478-129">OUTPUTS</span></span>

### <span data-ttu-id="0c478-130">VaultSettingsFilePath 中的 SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="0c478-130">Microsoft.Azure.Commands.SiteRecovery.VaultSettingsFilePath</span></span>

## <span data-ttu-id="0c478-131">筆記</span><span class="sxs-lookup"><span data-stu-id="0c478-131">NOTES</span></span>

## <span data-ttu-id="0c478-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="0c478-132">RELATED LINKS</span></span>

[<span data-ttu-id="0c478-133">匯入-AzureRmSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="0c478-133">Import-AzureRmSiteRecoveryVaultSettingsFile</span></span>](./Import-AzureRmSiteRecoveryVaultSettingsFile.md)

[<span data-ttu-id="0c478-134">Set-AzureRmSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="0c478-134">Set-AzureRmSiteRecoveryVaultSettings</span></span>](./Set-AzureRmSiteRecoveryVaultSettings.md)
