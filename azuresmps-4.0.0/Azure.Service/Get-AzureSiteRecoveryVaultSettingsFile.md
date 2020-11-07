---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: AFAA1BDF-3F6A-437A-ADC2-C5EBD970F57D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 94e86fdb7f1e995af71e09bdce17754b11819bec
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93968010"
---
# <span data-ttu-id="74061-101">Get-AzureSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="74061-101">Get-AzureSiteRecoveryVaultSettingsFile</span></span>

## <span data-ttu-id="74061-102">摘要</span><span class="sxs-lookup"><span data-stu-id="74061-102">SYNOPSIS</span></span>
<span data-ttu-id="74061-103">取得網站復原電子倉庫設定檔案。</span><span class="sxs-lookup"><span data-stu-id="74061-103">Gets the Site Recovery vault settings file.</span></span>

## <span data-ttu-id="74061-104">句法</span><span class="sxs-lookup"><span data-stu-id="74061-104">SYNTAX</span></span>

### <span data-ttu-id="74061-105">ByParam (預設) </span><span class="sxs-lookup"><span data-stu-id="74061-105">ByParam (Default)</span></span>
```
Get-AzureSiteRecoveryVaultSettingsFile -Name <String> -Location <String> [-SiteName <String>]
 [-SiteId <String>] [-Path <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="74061-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="74061-106">ByObject</span></span>
```
Get-AzureSiteRecoveryVaultSettingsFile -Vault <ASRVault> [-Site <ASRSite>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="74061-107">說明</span><span class="sxs-lookup"><span data-stu-id="74061-107">DESCRIPTION</span></span>
<span data-ttu-id="74061-108">**AzureSiteRecoveryVaultSettingsFile** Cmdlet 會取得 Azure Site Recovery 保存庫的設定檔案。</span><span class="sxs-lookup"><span data-stu-id="74061-108">The **Get-AzureSiteRecoveryVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="74061-109">示例</span><span class="sxs-lookup"><span data-stu-id="74061-109">EXAMPLES</span></span>

### <span data-ttu-id="74061-110">範例1：取得電子倉庫的設定檔</span><span class="sxs-lookup"><span data-stu-id="74061-110">Example 1: Get the settings file for a vault</span></span>
```
PS C:\> $Vault = Get-AzureSiteRecoveryVault -Name "ContosoVault"
PS C:\> Get-AzureSiteRecoveryVaultSettingsFile -Vault $Vault
FilePath 
-------- 
C:\Users\ContosoAdmin\ContosoVault_2015-02-02T05-39-23.VaultCredentials
```

<span data-ttu-id="74061-111">第一個命令會使用 **AzureSiteRecoveryVault** Cmdlet 取得名為 ContosoVault 的動態 Azure Site Recovery 保存庫。</span><span class="sxs-lookup"><span data-stu-id="74061-111">The first command gets the active Azure Site Recovery vault named ContosoVault by using the **Get-AzureSiteRecoveryVault** cmdlet.</span></span>
<span data-ttu-id="74061-112">該命令會將該電子倉庫儲存在 $Vault 變數中。</span><span class="sxs-lookup"><span data-stu-id="74061-112">The command stores that vault in the $Vault variable.</span></span>

<span data-ttu-id="74061-113">第二個命令會針對儲存在 $Vault 中的電子倉庫，取得設定檔案。</span><span class="sxs-lookup"><span data-stu-id="74061-113">The second command gets the settings file for the vault stored in $Vault.</span></span>

## <span data-ttu-id="74061-114">參數</span><span class="sxs-lookup"><span data-stu-id="74061-114">PARAMETERS</span></span>

### <span data-ttu-id="74061-115">-位置</span><span class="sxs-lookup"><span data-stu-id="74061-115">-Location</span></span>
<span data-ttu-id="74061-116">指定電子倉庫所屬的地理位置。</span><span class="sxs-lookup"><span data-stu-id="74061-116">Specifies the geographical location to which the vault belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74061-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="74061-117">-Name</span></span>
<span data-ttu-id="74061-118">指定電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="74061-118">Specifies the name of a vault.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74061-119">-Path</span><span class="sxs-lookup"><span data-stu-id="74061-119">-Path</span></span>
<span data-ttu-id="74061-120">指定網站復原電子倉庫設定檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="74061-120">Specifies the path of the Site Recovery vault settings file.</span></span>
<span data-ttu-id="74061-121">若要在本機儲存此檔案，請在命令完成執行之後，從網站復原電子倉庫入口網站下載。</span><span class="sxs-lookup"><span data-stu-id="74061-121">To store this file locally, download it from the Site Recovery vault portal after the command has finished running.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74061-122">-設定檔</span><span class="sxs-lookup"><span data-stu-id="74061-122">-Profile</span></span>
<span data-ttu-id="74061-123">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="74061-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="74061-124">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="74061-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74061-125">-網站</span><span class="sxs-lookup"><span data-stu-id="74061-125">-Site</span></span>
<span data-ttu-id="74061-126">指定要取得設定檔案的網站。</span><span class="sxs-lookup"><span data-stu-id="74061-126">Specifies a site for which to get a settings file.</span></span>
<span data-ttu-id="74061-127">若要取得 **網站** 物件，請使用 **AzureSiteRecoverySite** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="74061-127">To obtain a **Site** object, use the **Get-AzureSiteRecoverySite** cmdlet.</span></span>

```yaml
Type: ASRSite
Parameter Sets: ByObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74061-128">-SiteId</span><span class="sxs-lookup"><span data-stu-id="74061-128">-SiteId</span></span>
<span data-ttu-id="74061-129">指定網站的識別碼。</span><span class="sxs-lookup"><span data-stu-id="74061-129">Specifies the ID of a site.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74061-130">-SiteName</span><span class="sxs-lookup"><span data-stu-id="74061-130">-SiteName</span></span>
<span data-ttu-id="74061-131">指定網站的名稱。</span><span class="sxs-lookup"><span data-stu-id="74061-131">Specifies the name of a site.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74061-132">-保存庫</span><span class="sxs-lookup"><span data-stu-id="74061-132">-Vault</span></span>
<span data-ttu-id="74061-133">指定網站的電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="74061-133">Specifies the vault for the site.</span></span>

```yaml
Type: ASRVault
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74061-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74061-134">CommonParameters</span></span>
<span data-ttu-id="74061-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="74061-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74061-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="74061-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74061-137">輸入</span><span class="sxs-lookup"><span data-stu-id="74061-137">INPUTS</span></span>

## <span data-ttu-id="74061-138">輸出</span><span class="sxs-lookup"><span data-stu-id="74061-138">OUTPUTS</span></span>

## <span data-ttu-id="74061-139">筆記</span><span class="sxs-lookup"><span data-stu-id="74061-139">NOTES</span></span>

## <span data-ttu-id="74061-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="74061-140">RELATED LINKS</span></span>

[<span data-ttu-id="74061-141">AzureSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="74061-141">Get-AzureSiteRecoverySite</span></span>](./Get-AzureSiteRecoverySite.md)

[<span data-ttu-id="74061-142">AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="74061-142">Get-AzureSiteRecoveryVault</span></span>](./Get-AzureSiteRecoveryVault.md)

[<span data-ttu-id="74061-143">AzureSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="74061-143">Get-AzureSiteRecoveryVaultSettings</span></span>](./Get-AzureSiteRecoveryVaultSettings.md)

[<span data-ttu-id="74061-144">匯入-AzureSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="74061-144">Import-AzureSiteRecoveryVaultSettingsFile</span></span>](./Import-AzureSiteRecoveryVaultSettingsFile.md)


