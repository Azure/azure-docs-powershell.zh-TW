---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 56074606-28A6-4F91-A56C-4C8A9A31543F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/get-azurermrecoveryservicesvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVaultSettingsFile.md
ms.openlocfilehash: a0572e73d270a37b3c705018a38b4a88fe88d1e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455087"
---
# <span data-ttu-id="e72e1-101">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="e72e1-101">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>

## <span data-ttu-id="e72e1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e72e1-102">SYNOPSIS</span></span>
<span data-ttu-id="e72e1-103">取得 Azure Site Recovery 保存庫設定檔。</span><span class="sxs-lookup"><span data-stu-id="e72e1-103">Gets the Azure Site Recovery vault settings file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e72e1-104">句法</span><span class="sxs-lookup"><span data-stu-id="e72e1-104">SYNTAX</span></span>

### <span data-ttu-id="e72e1-105">ForSite</span><span class="sxs-lookup"><span data-stu-id="e72e1-105">ForSite</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> -SiteIdentifier <String>
 -SiteFriendlyName <String> [[-Path] <String>] [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e72e1-106">ByDefault</span><span class="sxs-lookup"><span data-stu-id="e72e1-106">ByDefault</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] [-SiteRecovery]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e72e1-107">ForBackupVaultType</span><span class="sxs-lookup"><span data-stu-id="e72e1-107">ForBackupVaultType</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] [-Backup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e72e1-108">說明</span><span class="sxs-lookup"><span data-stu-id="e72e1-108">DESCRIPTION</span></span>
<span data-ttu-id="e72e1-109">**AzureRmRecoveryServicesVaultSettingsFile** Cmdlet 會取得 Azure Site Recovery 保存庫的設定檔案。</span><span class="sxs-lookup"><span data-stu-id="e72e1-109">The **Get-AzureRmRecoveryServicesVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="e72e1-110">示例</span><span class="sxs-lookup"><span data-stu-id="e72e1-110">EXAMPLES</span></span>

### <span data-ttu-id="e72e1-111">範例1：針對 Azure 備份註冊 Windows Server 或 DPM 電腦</span><span class="sxs-lookup"><span data-stu-id="e72e1-111">Example 1: Register a Windows Server or DPM machine for Azure Backup</span></span>
```
PS C:\> $Vault01 = Get-AzureRmRecoveryServicesVault -Name "TestVault"
PS C:\> $CredsPath = "C:\Downloads"
PS C:\> $Credsfilename = Get-AzureRmRecoveryServicesVaultSettingsFile -Backup -Vault $Vault01 -Path $CredsPath
```

<span data-ttu-id="e72e1-112">第一個命令會取得名為 TestVault 的電子倉庫，然後將它儲存在 $Vault 01 變數中。</span><span class="sxs-lookup"><span data-stu-id="e72e1-112">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>
<span data-ttu-id="e72e1-113">第二個命令會將 $CredsPath 變數設定為 C:\Downloads。</span><span class="sxs-lookup"><span data-stu-id="e72e1-113">The second command sets the $CredsPath variable to C:\Downloads.</span></span>
<span data-ttu-id="e72e1-114">最後一個命令會使用 Azure 備份 $CredsPath 中的認證來取得 $Vault 01 的保存庫認證檔案。</span><span class="sxs-lookup"><span data-stu-id="e72e1-114">The last command gets the vault credentials file for $Vault01 using the credentials in $CredsPath for Azure Backup.</span></span>

### <span data-ttu-id="e72e1-115">範例2：</span><span class="sxs-lookup"><span data-stu-id="e72e1-115">Example 2:</span></span>
```
PS C:\> $Credsfilename = Get-AzureRmRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="e72e1-116">此命令會取得 $Vault 01 siteRecovery vault 類型的保存庫認證檔案。</span><span class="sxs-lookup"><span data-stu-id="e72e1-116">The command gets the vault credentials file for $Vault01 of vault type siteRecovery.</span></span>

### <span data-ttu-id="e72e1-117">範例3：針對 Azure 備份註冊 Windows Server 或 DPM 電腦</span><span class="sxs-lookup"><span data-stu-id="e72e1-117">Example 3: Register a Windows Server or DPM machine for Azure Backup</span></span>
```
PS C:\> $Credsfilename = Get-AzureRmRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="e72e1-118">此命令會取得 $Vault 01 的保存庫認證檔案。</span><span class="sxs-lookup"><span data-stu-id="e72e1-118">The command gets the vault credentials file for $Vault01.</span></span>

## <span data-ttu-id="e72e1-119">參數</span><span class="sxs-lookup"><span data-stu-id="e72e1-119">PARAMETERS</span></span>

### <span data-ttu-id="e72e1-120">-備份</span><span class="sxs-lookup"><span data-stu-id="e72e1-120">-Backup</span></span>
<span data-ttu-id="e72e1-121">表示保存庫認證檔案適用于 Azure 備份。</span><span class="sxs-lookup"><span data-stu-id="e72e1-121">Indicates the vault credentials file is applicable to Azure Backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForBackupVaultType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e72e1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e72e1-122">-DefaultProfile</span></span>
<span data-ttu-id="e72e1-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e72e1-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e72e1-124">-Path</span><span class="sxs-lookup"><span data-stu-id="e72e1-124">-Path</span></span>
<span data-ttu-id="e72e1-125">指定 Azure Site Recovery 保存庫設定檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="e72e1-125">Specifies the path to the Azure Site Recovery vault settings file.</span></span>
<span data-ttu-id="e72e1-126">您可以從 Azure Site Recovery 保存庫入口網站下載此檔案，並將它儲存在本機。</span><span class="sxs-lookup"><span data-stu-id="e72e1-126">You can download this file from the Azure Site Recovery vault portal and store it locally.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e72e1-127">-SiteFriendlyName</span><span class="sxs-lookup"><span data-stu-id="e72e1-127">-SiteFriendlyName</span></span>
<span data-ttu-id="e72e1-128">指定網站的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="e72e1-128">Specifies the site friendly name.</span></span>
<span data-ttu-id="e72e1-129">如果您要下載 Hyper-v 網站的保存庫認證，請使用此參數。</span><span class="sxs-lookup"><span data-stu-id="e72e1-129">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

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

### <span data-ttu-id="e72e1-130">-SiteIdentifier</span><span class="sxs-lookup"><span data-stu-id="e72e1-130">-SiteIdentifier</span></span>
<span data-ttu-id="e72e1-131">指定網站識別碼。</span><span class="sxs-lookup"><span data-stu-id="e72e1-131">Specifies the site identifier.</span></span>
<span data-ttu-id="e72e1-132">如果您要下載 Hyper-v 網站的保存庫認證，請使用此參數。</span><span class="sxs-lookup"><span data-stu-id="e72e1-132">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

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

### <span data-ttu-id="e72e1-133">-SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="e72e1-133">-SiteRecovery</span></span>
<span data-ttu-id="e72e1-134">表示保存庫認證檔案適用于 Azure Site Recovery。</span><span class="sxs-lookup"><span data-stu-id="e72e1-134">Indicates the vault credentials file is applicable to Azure Site Recovery.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForSite, ByDefault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e72e1-135">-保存庫</span><span class="sxs-lookup"><span data-stu-id="e72e1-135">-Vault</span></span>
<span data-ttu-id="e72e1-136">指定 Azure Site Recovery 保存庫物件。</span><span class="sxs-lookup"><span data-stu-id="e72e1-136">Specifies the Azure Site Recovery vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e72e1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e72e1-137">CommonParameters</span></span>
<span data-ttu-id="e72e1-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e72e1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e72e1-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e72e1-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e72e1-140">輸入</span><span class="sxs-lookup"><span data-stu-id="e72e1-140">INPUTS</span></span>

### <span data-ttu-id="e72e1-141">ARSVault 中的 RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e72e1-141">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>
<span data-ttu-id="e72e1-142">參數：保存庫 (ByValue) </span><span class="sxs-lookup"><span data-stu-id="e72e1-142">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="e72e1-143">輸出</span><span class="sxs-lookup"><span data-stu-id="e72e1-143">OUTPUTS</span></span>

### <span data-ttu-id="e72e1-144">VaultSettingsFilePath 中的 RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e72e1-144">Microsoft.Azure.Commands.RecoveryServices.VaultSettingsFilePath</span></span>

## <span data-ttu-id="e72e1-145">筆記</span><span class="sxs-lookup"><span data-stu-id="e72e1-145">NOTES</span></span>

## <span data-ttu-id="e72e1-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="e72e1-146">RELATED LINKS</span></span>

[<span data-ttu-id="e72e1-147">AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="e72e1-147">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="e72e1-148">新-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="e72e1-148">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="e72e1-149">移除-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="e72e1-149">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


