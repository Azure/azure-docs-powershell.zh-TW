---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 56074606-28A6-4F91-A56C-4C8A9A31543F
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultSettingsFile.md
ms.openlocfilehash: b71da123933cd190038164b67d37fb81b0d5c973
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915249"
---
# <span data-ttu-id="3a5aa-101">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="3a5aa-101">Get-AzRecoveryServicesVaultSettingsFile</span></span>

## <span data-ttu-id="3a5aa-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3a5aa-102">SYNOPSIS</span></span>
<span data-ttu-id="3a5aa-103">獲得 Azure 網站修復保存庫設定檔案。</span><span class="sxs-lookup"><span data-stu-id="3a5aa-103">Gets the Azure Site Recovery vault settings file.</span></span>

## <span data-ttu-id="3a5aa-104">語法</span><span class="sxs-lookup"><span data-stu-id="3a5aa-104">SYNTAX</span></span>

### <span data-ttu-id="3a5aa-105">ForSiteWithCertificate</span><span class="sxs-lookup"><span data-stu-id="3a5aa-105">ForSiteWithCertificate</span></span>
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -SiteIdentifier <String>
 -Certificate <String> -SiteFriendlyName <String> [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3a5aa-106">ByDefaultWithCertificate</span><span class="sxs-lookup"><span data-stu-id="3a5aa-106">ByDefaultWithCertificate</span></span>
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -Certificate <String>
 [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a5aa-107">ForBackupVaultTypeWithCertificate</span><span class="sxs-lookup"><span data-stu-id="3a5aa-107">ForBackupVaultTypeWithCertificate</span></span>
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -Certificate <String> [-Backup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a5aa-108">描述</span><span class="sxs-lookup"><span data-stu-id="3a5aa-108">DESCRIPTION</span></span>
<span data-ttu-id="3a5aa-109">**Get-AzRecoveryServicesVaultSettingsFile** Cmdlet 會取得 Azure 網站修復保存庫的設定檔案。</span><span class="sxs-lookup"><span data-stu-id="3a5aa-109">The **Get-AzRecoveryServicesVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="3a5aa-110">例子</span><span class="sxs-lookup"><span data-stu-id="3a5aa-110">EXAMPLES</span></span>

### <span data-ttu-id="3a5aa-111">範例 1：註冊適用于 Azure 備份的 Windows Server 或 DPM 電腦</span><span class="sxs-lookup"><span data-stu-id="3a5aa-111">Example 1: Register a Windows Server or DPM machine for Azure Backup</span></span>
```powershell
PS C:\> $Vault01 = Get-AzRecoveryServicesVault -Name "TestVault"
PS C:\> $CredsPath = "C:\Downloads"
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -Backup -Vault $Vault01 -Path $CredsPath
```

<span data-ttu-id="3a5aa-112">第一個命令會獲得名為 TestVault 的保存庫，然後將它儲存在 $Vault 01 變數中。</span><span class="sxs-lookup"><span data-stu-id="3a5aa-112">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>
<span data-ttu-id="3a5aa-113">第二個命令將 $CredsPath變數設定為 C：\Downloads。</span><span class="sxs-lookup"><span data-stu-id="3a5aa-113">The second command sets the $CredsPath variable to C:\Downloads.</span></span>
<span data-ttu-id="3a5aa-114">最後一個命令會使用 Azure 備份$Vault 01 中的認證來$CredsPath保存庫認證檔案。</span><span class="sxs-lookup"><span data-stu-id="3a5aa-114">The last command gets the vault credentials file for $Vault01 using the credentials in $CredsPath for Azure Backup.</span></span>

### <span data-ttu-id="3a5aa-115">範例 2</span><span class="sxs-lookup"><span data-stu-id="3a5aa-115">Example 2</span></span>
```powershell
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="3a5aa-116">該命令會獲得保存庫類型網站Recovery $Vault 01 的保存庫認證檔案。</span><span class="sxs-lookup"><span data-stu-id="3a5aa-116">The command gets the vault credentials file for $Vault01 of vault type siteRecovery.</span></span>

### <span data-ttu-id="3a5aa-117">範例 3：註冊適用于 Azure 備份的 Windows Server 或 DPM 電腦</span><span class="sxs-lookup"><span data-stu-id="3a5aa-117">Example 3: Register a Windows Server or DPM machine for Azure Backup</span></span>
```powershell
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="3a5aa-118">該命令會獲得 $Vault 01 的保存庫認證檔案。</span><span class="sxs-lookup"><span data-stu-id="3a5aa-118">The command gets the vault credentials file for $Vault01.</span></span>

## <span data-ttu-id="3a5aa-119">參數</span><span class="sxs-lookup"><span data-stu-id="3a5aa-119">PARAMETERS</span></span>

### <span data-ttu-id="3a5aa-120">-備份</span><span class="sxs-lookup"><span data-stu-id="3a5aa-120">-Backup</span></span>
<span data-ttu-id="3a5aa-121">表示保存庫認證檔案適用于 Azure 備份。</span><span class="sxs-lookup"><span data-stu-id="3a5aa-121">Indicates the vault credentials file is applicable to Azure Backup.</span></span>

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

### <span data-ttu-id="3a5aa-122">-憑證</span><span class="sxs-lookup"><span data-stu-id="3a5aa-122">-Certificate</span></span>
<span data-ttu-id="3a5aa-123">{{Fill Certificate Description}}</span><span class="sxs-lookup"><span data-stu-id="3a5aa-123">{{Fill Certificate Description}}</span></span>

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

### <span data-ttu-id="3a5aa-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a5aa-124">-DefaultProfile</span></span>
<span data-ttu-id="3a5aa-125">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3a5aa-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a5aa-126">-路徑</span><span class="sxs-lookup"><span data-stu-id="3a5aa-126">-Path</span></span>
<span data-ttu-id="3a5aa-127">指定 Azure 網站復原保存庫設定檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="3a5aa-127">Specifies the path to the Azure Site Recovery vault settings file.</span></span>
<span data-ttu-id="3a5aa-128">您可以從 Azure 網站修復保存庫入口網站下載此檔案，並儲存在本地。</span><span class="sxs-lookup"><span data-stu-id="3a5aa-128">You can download this file from the Azure Site Recovery vault portal and store it locally.</span></span>

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

### <span data-ttu-id="3a5aa-129">-Site1LyName</span><span class="sxs-lookup"><span data-stu-id="3a5aa-129">-SiteFriendlyName</span></span>
<span data-ttu-id="3a5aa-130">指定網站好用的名稱。</span><span class="sxs-lookup"><span data-stu-id="3a5aa-130">Specifies the site friendly name.</span></span>
<span data-ttu-id="3a5aa-131">如果您要下載 Hyper-V 網站的保存庫認證，請使用此參數。</span><span class="sxs-lookup"><span data-stu-id="3a5aa-131">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

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

### <span data-ttu-id="3a5aa-132">-SiteIdentifier</span><span class="sxs-lookup"><span data-stu-id="3a5aa-132">-SiteIdentifier</span></span>
<span data-ttu-id="3a5aa-133">指定網站識別碼。</span><span class="sxs-lookup"><span data-stu-id="3a5aa-133">Specifies the site identifier.</span></span>
<span data-ttu-id="3a5aa-134">如果您要下載 Hyper-V 網站的保存庫認證，請使用此參數。</span><span class="sxs-lookup"><span data-stu-id="3a5aa-134">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

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

### <span data-ttu-id="3a5aa-135">-SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="3a5aa-135">-SiteRecovery</span></span>
<span data-ttu-id="3a5aa-136">表示保存庫認證檔案適用于 Azure 網站復原。</span><span class="sxs-lookup"><span data-stu-id="3a5aa-136">Indicates the vault credentials file is applicable to Azure Site Recovery.</span></span>

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

### <span data-ttu-id="3a5aa-137">-Vault</span><span class="sxs-lookup"><span data-stu-id="3a5aa-137">-Vault</span></span>
<span data-ttu-id="3a5aa-138">指定 Azure 網站修復庫物件。</span><span class="sxs-lookup"><span data-stu-id="3a5aa-138">Specifies the Azure Site Recovery vault object.</span></span>

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

### <span data-ttu-id="3a5aa-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a5aa-139">CommonParameters</span></span>
<span data-ttu-id="3a5aa-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3a5aa-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a5aa-141">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3a5aa-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a5aa-142">輸入</span><span class="sxs-lookup"><span data-stu-id="3a5aa-142">INPUTS</span></span>

### <span data-ttu-id="3a5aa-143">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="3a5aa-143">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="3a5aa-144">輸出</span><span class="sxs-lookup"><span data-stu-id="3a5aa-144">OUTPUTS</span></span>

### <span data-ttu-id="3a5aa-145">Microsoft.Azure.Commands.RecoveryServices.VaultSettingsFilePath</span><span class="sxs-lookup"><span data-stu-id="3a5aa-145">Microsoft.Azure.Commands.RecoveryServices.VaultSettingsFilePath</span></span>

## <span data-ttu-id="3a5aa-146">筆記</span><span class="sxs-lookup"><span data-stu-id="3a5aa-146">NOTES</span></span>

## <span data-ttu-id="3a5aa-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="3a5aa-147">RELATED LINKS</span></span>

[<span data-ttu-id="3a5aa-148">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="3a5aa-148">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="3a5aa-149">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="3a5aa-149">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

[<span data-ttu-id="3a5aa-150">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="3a5aa-150">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)


