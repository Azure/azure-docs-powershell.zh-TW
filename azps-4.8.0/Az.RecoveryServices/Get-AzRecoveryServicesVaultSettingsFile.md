---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 56074606-28A6-4F91-A56C-4C8A9A31543F
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultSettingsFile.md
ms.openlocfilehash: 0d074c18ad9b5f9ea34a465acd4a91a88d4b69ac
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969137"
---
# <span data-ttu-id="ad4c2-101">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="ad4c2-101">Get-AzRecoveryServicesVaultSettingsFile</span></span>

## <span data-ttu-id="ad4c2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ad4c2-102">SYNOPSIS</span></span>
<span data-ttu-id="ad4c2-103">取得 Azure Site Recovery 保存庫設定檔。</span><span class="sxs-lookup"><span data-stu-id="ad4c2-103">Gets the Azure Site Recovery vault settings file.</span></span>

## <span data-ttu-id="ad4c2-104">句法</span><span class="sxs-lookup"><span data-stu-id="ad4c2-104">SYNTAX</span></span>

### <span data-ttu-id="ad4c2-105">ForSiteWithCertificate</span><span class="sxs-lookup"><span data-stu-id="ad4c2-105">ForSiteWithCertificate</span></span>
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -SiteIdentifier <String>
 -Certificate <String> -SiteFriendlyName <String> [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ad4c2-106">ByDefaultWithCertificate</span><span class="sxs-lookup"><span data-stu-id="ad4c2-106">ByDefaultWithCertificate</span></span>
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -Certificate <String>
 [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ad4c2-107">ForBackupVaultTypeWithCertificate</span><span class="sxs-lookup"><span data-stu-id="ad4c2-107">ForBackupVaultTypeWithCertificate</span></span>
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -Certificate <String> [-Backup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad4c2-108">說明</span><span class="sxs-lookup"><span data-stu-id="ad4c2-108">DESCRIPTION</span></span>
<span data-ttu-id="ad4c2-109">**AzRecoveryServicesVaultSettingsFile** Cmdlet 會取得 Azure Site Recovery 保存庫的設定檔案。</span><span class="sxs-lookup"><span data-stu-id="ad4c2-109">The **Get-AzRecoveryServicesVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="ad4c2-110">示例</span><span class="sxs-lookup"><span data-stu-id="ad4c2-110">EXAMPLES</span></span>

### <span data-ttu-id="ad4c2-111">範例1：針對 Azure 備份註冊 Windows Server 或 DPM 電腦</span><span class="sxs-lookup"><span data-stu-id="ad4c2-111">Example 1: Register a Windows Server or DPM machine for Azure Backup</span></span>
```powershell
PS C:\> $Vault01 = Get-AzRecoveryServicesVault -Name "TestVault"
PS C:\> $CredsPath = "C:\Downloads"
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -Backup -Vault $Vault01 -Path $CredsPath
```

<span data-ttu-id="ad4c2-112">第一個命令會取得名為 TestVault 的電子倉庫，然後將它儲存在 $Vault 01 變數中。</span><span class="sxs-lookup"><span data-stu-id="ad4c2-112">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>
<span data-ttu-id="ad4c2-113">第二個命令會將 $CredsPath 變數設定為 C:\Downloads。</span><span class="sxs-lookup"><span data-stu-id="ad4c2-113">The second command sets the $CredsPath variable to C:\Downloads.</span></span>
<span data-ttu-id="ad4c2-114">最後一個命令會使用 Azure 備份 $CredsPath 中的認證來取得 $Vault 01 的保存庫認證檔案。</span><span class="sxs-lookup"><span data-stu-id="ad4c2-114">The last command gets the vault credentials file for $Vault01 using the credentials in $CredsPath for Azure Backup.</span></span>

### <span data-ttu-id="ad4c2-115">範例2</span><span class="sxs-lookup"><span data-stu-id="ad4c2-115">Example 2</span></span>
```powershell
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="ad4c2-116">此命令會取得 $Vault 01 siteRecovery vault 類型的保存庫認證檔案。</span><span class="sxs-lookup"><span data-stu-id="ad4c2-116">The command gets the vault credentials file for $Vault01 of vault type siteRecovery.</span></span>

### <span data-ttu-id="ad4c2-117">範例3：針對 Azure 備份註冊 Windows Server 或 DPM 電腦</span><span class="sxs-lookup"><span data-stu-id="ad4c2-117">Example 3: Register a Windows Server or DPM machine for Azure Backup</span></span>
```powershell
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="ad4c2-118">此命令會取得 $Vault 01 的保存庫認證檔案。</span><span class="sxs-lookup"><span data-stu-id="ad4c2-118">The command gets the vault credentials file for $Vault01.</span></span>

## <span data-ttu-id="ad4c2-119">參數</span><span class="sxs-lookup"><span data-stu-id="ad4c2-119">PARAMETERS</span></span>

### <span data-ttu-id="ad4c2-120">-備份</span><span class="sxs-lookup"><span data-stu-id="ad4c2-120">-Backup</span></span>
<span data-ttu-id="ad4c2-121">表示保存庫認證檔案適用于 Azure 備份。</span><span class="sxs-lookup"><span data-stu-id="ad4c2-121">Indicates the vault credentials file is applicable to Azure Backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForBackupVaultTypeWithCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad4c2-122">-Certificate</span><span class="sxs-lookup"><span data-stu-id="ad4c2-122">-Certificate</span></span>
<span data-ttu-id="ad4c2-123">{{Fill 證書描述}}</span><span class="sxs-lookup"><span data-stu-id="ad4c2-123">{{Fill Certificate Description}}</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad4c2-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad4c2-124">-DefaultProfile</span></span>
<span data-ttu-id="ad4c2-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ad4c2-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad4c2-126">-Path</span><span class="sxs-lookup"><span data-stu-id="ad4c2-126">-Path</span></span>
<span data-ttu-id="ad4c2-127">指定 Azure Site Recovery 保存庫設定檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="ad4c2-127">Specifies the path to the Azure Site Recovery vault settings file.</span></span>
<span data-ttu-id="ad4c2-128">您可以從 Azure Site Recovery 保存庫入口網站下載此檔案，並將它儲存在本機。</span><span class="sxs-lookup"><span data-stu-id="ad4c2-128">You can download this file from the Azure Site Recovery vault portal and store it locally.</span></span>

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

### <span data-ttu-id="ad4c2-129">-SiteFriendlyName</span><span class="sxs-lookup"><span data-stu-id="ad4c2-129">-SiteFriendlyName</span></span>
<span data-ttu-id="ad4c2-130">指定網站的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="ad4c2-130">Specifies the site friendly name.</span></span>
<span data-ttu-id="ad4c2-131">如果您要下載 Hyper-v 網站的保存庫認證，請使用此參數。</span><span class="sxs-lookup"><span data-stu-id="ad4c2-131">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

```yaml
Type: System.String
Parameter Sets: ForSiteWithCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad4c2-132">-SiteIdentifier</span><span class="sxs-lookup"><span data-stu-id="ad4c2-132">-SiteIdentifier</span></span>
<span data-ttu-id="ad4c2-133">指定網站識別碼。</span><span class="sxs-lookup"><span data-stu-id="ad4c2-133">Specifies the site identifier.</span></span>
<span data-ttu-id="ad4c2-134">如果您要下載 Hyper-v 網站的保存庫認證，請使用此參數。</span><span class="sxs-lookup"><span data-stu-id="ad4c2-134">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

```yaml
Type: System.String
Parameter Sets: ForSiteWithCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad4c2-135">-SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="ad4c2-135">-SiteRecovery</span></span>
<span data-ttu-id="ad4c2-136">表示保存庫認證檔案適用于 Azure Site Recovery。</span><span class="sxs-lookup"><span data-stu-id="ad4c2-136">Indicates the vault credentials file is applicable to Azure Site Recovery.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForSiteWithCertificate, ByDefaultWithCertificate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad4c2-137">-保存庫</span><span class="sxs-lookup"><span data-stu-id="ad4c2-137">-Vault</span></span>
<span data-ttu-id="ad4c2-138">指定 Azure Site Recovery 保存庫物件。</span><span class="sxs-lookup"><span data-stu-id="ad4c2-138">Specifies the Azure Site Recovery vault object.</span></span>

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

### <span data-ttu-id="ad4c2-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad4c2-139">CommonParameters</span></span>
<span data-ttu-id="ad4c2-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ad4c2-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad4c2-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ad4c2-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad4c2-142">輸入</span><span class="sxs-lookup"><span data-stu-id="ad4c2-142">INPUTS</span></span>

### <span data-ttu-id="ad4c2-143">ARSVault 中的 RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ad4c2-143">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="ad4c2-144">輸出</span><span class="sxs-lookup"><span data-stu-id="ad4c2-144">OUTPUTS</span></span>

### <span data-ttu-id="ad4c2-145">VaultSettingsFilePath 中的 RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ad4c2-145">Microsoft.Azure.Commands.RecoveryServices.VaultSettingsFilePath</span></span>

## <span data-ttu-id="ad4c2-146">筆記</span><span class="sxs-lookup"><span data-stu-id="ad4c2-146">NOTES</span></span>

## <span data-ttu-id="ad4c2-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="ad4c2-147">RELATED LINKS</span></span>

[<span data-ttu-id="ad4c2-148">AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="ad4c2-148">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="ad4c2-149">新-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="ad4c2-149">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

[<span data-ttu-id="ad4c2-150">移除-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="ad4c2-150">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)


