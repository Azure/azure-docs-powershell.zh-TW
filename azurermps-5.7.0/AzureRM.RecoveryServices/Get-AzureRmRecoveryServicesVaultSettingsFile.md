---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 56074606-28A6-4F91-A56C-4C8A9A31543F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/get-azurermrecoveryservicesvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVaultSettingsFile.md
ms.openlocfilehash: b272f22c0bac37f5318deff50f1f0b56a849ce2d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625004"
---
# <span data-ttu-id="7e33f-101">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="7e33f-101">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>

## <span data-ttu-id="7e33f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7e33f-102">SYNOPSIS</span></span>
<span data-ttu-id="7e33f-103">取得 Azure Site Recovery 保存庫設定檔。</span><span class="sxs-lookup"><span data-stu-id="7e33f-103">Gets the Azure Site Recovery vault settings file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e33f-104">句法</span><span class="sxs-lookup"><span data-stu-id="7e33f-104">SYNTAX</span></span>

### <span data-ttu-id="7e33f-105">ForSite</span><span class="sxs-lookup"><span data-stu-id="7e33f-105">ForSite</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> -SiteIdentifier <String>
 -SiteFriendlyName <String> [[-Path] <String>] [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7e33f-106">ByDefault</span><span class="sxs-lookup"><span data-stu-id="7e33f-106">ByDefault</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] [-SiteRecovery]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e33f-107">ForBackupVaultType</span><span class="sxs-lookup"><span data-stu-id="7e33f-107">ForBackupVaultType</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] [-Backup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e33f-108">說明</span><span class="sxs-lookup"><span data-stu-id="7e33f-108">DESCRIPTION</span></span>
<span data-ttu-id="7e33f-109">**AzureRmRecoveryServicesVaultSettingsFile** Cmdlet 會取得 Azure Site Recovery 保存庫的設定檔案。</span><span class="sxs-lookup"><span data-stu-id="7e33f-109">The **Get-AzureRmRecoveryServicesVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="7e33f-110">示例</span><span class="sxs-lookup"><span data-stu-id="7e33f-110">EXAMPLES</span></span>

### <span data-ttu-id="7e33f-111">範例1：針對 Azure 備份註冊 Windows Server 或 DPM 電腦</span><span class="sxs-lookup"><span data-stu-id="7e33f-111">Example 1: Register a Windows Server or DPM machine for Azure Backup</span></span>
```
PS C:\> $Vault01 = Get-AzureRmRecoveryServicesVault -Name "TestVault"
PS C:\> $CredsPath = "C:\Downloads"
PS C:\> $Credsfilename = Get-AzureRmRecoveryServicesVaultSettingsFile -Backup -Vault $Vault01 -Path $CredsPath
```

<span data-ttu-id="7e33f-112">第一個命令會取得名為 TestVault 的電子倉庫，然後將它儲存在 $Vault 01 變數中。</span><span class="sxs-lookup"><span data-stu-id="7e33f-112">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>

<span data-ttu-id="7e33f-113">第二個命令會將 $CredsPath 變數設定為 C:\Downloads。</span><span class="sxs-lookup"><span data-stu-id="7e33f-113">The second command sets the $CredsPath variable to C:\Downloads.</span></span>

<span data-ttu-id="7e33f-114">最後一個命令會使用 Azure 備份 $CredsPath 中的認證來取得 $Vault 01 的保存庫認證檔案。</span><span class="sxs-lookup"><span data-stu-id="7e33f-114">The last command gets the vault credentials file for $Vault01 using the credentials in $CredsPath for Azure Backup.</span></span>

### <span data-ttu-id="7e33f-115">範例2：</span><span class="sxs-lookup"><span data-stu-id="7e33f-115">Example 2:</span></span>
```
PS C:\> $Credsfilename = Get-AzureRmRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="7e33f-116">此命令會取得 $Vault 01 siteRecovery vault 類型的保存庫認證檔案。</span><span class="sxs-lookup"><span data-stu-id="7e33f-116">The command gets the vault credentials file for $Vault01 of vault type siteRecovery.</span></span>

### <span data-ttu-id="7e33f-117">範例3：針對 Azure 備份註冊 Windows Server 或 DPM 電腦</span><span class="sxs-lookup"><span data-stu-id="7e33f-117">Example 3: Register a Windows Server or DPM machine for Azure Backup</span></span>
```
PS C:\> $Credsfilename = Get-AzureRmRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="7e33f-118">此命令會取得 $Vault 01 的保存庫認證檔案。</span><span class="sxs-lookup"><span data-stu-id="7e33f-118">The command gets the vault credentials file for $Vault01.</span></span>

## <span data-ttu-id="7e33f-119">參數</span><span class="sxs-lookup"><span data-stu-id="7e33f-119">PARAMETERS</span></span>

### <span data-ttu-id="7e33f-120">-備份</span><span class="sxs-lookup"><span data-stu-id="7e33f-120">-Backup</span></span>
<span data-ttu-id="7e33f-121">表示保存庫認證檔案適用于 Azure 備份。</span><span class="sxs-lookup"><span data-stu-id="7e33f-121">Indicates the vault credentials file is applicable to Azure Backup.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForBackupVaultType
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e33f-122">-Path</span><span class="sxs-lookup"><span data-stu-id="7e33f-122">-Path</span></span>
<span data-ttu-id="7e33f-123">指定 Azure Site Recovery 保存庫設定檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="7e33f-123">Specifies the path to the Azure Site Recovery vault settings file.</span></span>
<span data-ttu-id="7e33f-124">您可以從 Azure Site Recovery 保存庫入口網站下載此檔案，並將它儲存在本機。</span><span class="sxs-lookup"><span data-stu-id="7e33f-124">You can download this file from the Azure Site Recovery vault portal and store it locally.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e33f-125">-SiteFriendlyName</span><span class="sxs-lookup"><span data-stu-id="7e33f-125">-SiteFriendlyName</span></span>
<span data-ttu-id="7e33f-126">指定網站的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="7e33f-126">Specifies the site friendly name.</span></span>
<span data-ttu-id="7e33f-127">如果您要下載 Hyper-v 網站的保存庫認證，請使用此參數。</span><span class="sxs-lookup"><span data-stu-id="7e33f-127">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

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

### <span data-ttu-id="7e33f-128">-SiteIdentifier</span><span class="sxs-lookup"><span data-stu-id="7e33f-128">-SiteIdentifier</span></span>
<span data-ttu-id="7e33f-129">指定網站識別碼。</span><span class="sxs-lookup"><span data-stu-id="7e33f-129">Specifies the site identifier.</span></span>
<span data-ttu-id="7e33f-130">如果您要下載 Hyper-v 網站的保存庫認證，請使用此參數。</span><span class="sxs-lookup"><span data-stu-id="7e33f-130">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

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

### <span data-ttu-id="7e33f-131">-SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="7e33f-131">-SiteRecovery</span></span>
<span data-ttu-id="7e33f-132">表示保存庫認證檔案適用于 Azure Site Recovery。</span><span class="sxs-lookup"><span data-stu-id="7e33f-132">Indicates the vault credentials file is applicable to Azure Site Recovery.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForSite, ByDefault
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e33f-133">-保存庫</span><span class="sxs-lookup"><span data-stu-id="7e33f-133">-Vault</span></span>
<span data-ttu-id="7e33f-134">指定 Azure Site Recovery 保存庫物件。</span><span class="sxs-lookup"><span data-stu-id="7e33f-134">Specifies the Azure Site Recovery vault object.</span></span>

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e33f-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e33f-135">-DefaultProfile</span></span>
<span data-ttu-id="7e33f-136">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7e33f-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e33f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e33f-137">CommonParameters</span></span>
<span data-ttu-id="7e33f-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7e33f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e33f-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7e33f-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e33f-140">輸入</span><span class="sxs-lookup"><span data-stu-id="7e33f-140">INPUTS</span></span>

### <span data-ttu-id="7e33f-141">ARSVault</span><span class="sxs-lookup"><span data-stu-id="7e33f-141">ARSVault</span></span>
<span data-ttu-id="7e33f-142">參數 "Vault" 接受來自管線的 "ARSVault" 類型值</span><span class="sxs-lookup"><span data-stu-id="7e33f-142">Parameter 'Vault' accepts value of type 'ARSVault' from the pipeline</span></span>

## <span data-ttu-id="7e33f-143">輸出</span><span class="sxs-lookup"><span data-stu-id="7e33f-143">OUTPUTS</span></span>

### <span data-ttu-id="7e33f-144">VaultSettingsFilePath 中的 RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7e33f-144">Microsoft.Azure.Commands.RecoveryServices.VaultSettingsFilePath</span></span>

## <span data-ttu-id="7e33f-145">筆記</span><span class="sxs-lookup"><span data-stu-id="7e33f-145">NOTES</span></span>

## <span data-ttu-id="7e33f-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="7e33f-146">RELATED LINKS</span></span>

[<span data-ttu-id="7e33f-147">AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="7e33f-147">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="7e33f-148">新-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="7e33f-148">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="7e33f-149">移除-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="7e33f-149">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


