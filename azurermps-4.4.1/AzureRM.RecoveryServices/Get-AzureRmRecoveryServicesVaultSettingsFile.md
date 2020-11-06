---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 56074606-28A6-4F91-A56C-4C8A9A31543F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVaultSettingsFile.md
ms.openlocfilehash: 603cd65195f9e33c5006dcb4f2dc98ffc64aa7a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453307"
---
# <span data-ttu-id="8f7fa-101">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="8f7fa-101">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>

## <span data-ttu-id="8f7fa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8f7fa-102">SYNOPSIS</span></span>
<span data-ttu-id="8f7fa-103">取得 Azure Site Recovery 保存庫設定檔。</span><span class="sxs-lookup"><span data-stu-id="8f7fa-103">Gets the Azure Site Recovery vault settings file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f7fa-104">句法</span><span class="sxs-lookup"><span data-stu-id="8f7fa-104">SYNTAX</span></span>

### <span data-ttu-id="8f7fa-105">ForSite</span><span class="sxs-lookup"><span data-stu-id="8f7fa-105">ForSite</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> -SiteIdentifier <String>
 -SiteFriendlyName <String> [[-Path] <String>] [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8f7fa-106">ByDefault</span><span class="sxs-lookup"><span data-stu-id="8f7fa-106">ByDefault</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] [-SiteRecovery]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f7fa-107">ForBackupVaultType</span><span class="sxs-lookup"><span data-stu-id="8f7fa-107">ForBackupVaultType</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] [-Backup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f7fa-108">說明</span><span class="sxs-lookup"><span data-stu-id="8f7fa-108">DESCRIPTION</span></span>
<span data-ttu-id="8f7fa-109">**AzureRmRecoveryServicesVaultSettingsFile** Cmdlet 會取得 Azure Site Recovery 保存庫的設定檔案。</span><span class="sxs-lookup"><span data-stu-id="8f7fa-109">The **Get-AzureRmRecoveryServicesVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="8f7fa-110">示例</span><span class="sxs-lookup"><span data-stu-id="8f7fa-110">EXAMPLES</span></span>

### <span data-ttu-id="8f7fa-111">範例1：針對 Azure 備份註冊 Windows Server 或 DPM 電腦</span><span class="sxs-lookup"><span data-stu-id="8f7fa-111">Example 1: Register a Windows Server or DPM machine for Azure Backup</span></span>
```
PS C:\> $Vault01 = Get-AzureRmRecoveryServicesVault -Name "TestVault"
PS C:\> $CredsPath = "C:\Downloads"
PS C:\> $Credsfilename = Get-AzureRmRecoveryServicesVaultSettingsFile -Backup -Vault $Vault01 -Path $CredsPath
```

<span data-ttu-id="8f7fa-112">第一個命令會取得名為 TestVault 的電子倉庫，然後將它儲存在 $Vault 01 變數中。</span><span class="sxs-lookup"><span data-stu-id="8f7fa-112">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>

<span data-ttu-id="8f7fa-113">第二個命令會將 $CredsPath 變數設定為 C:\Downloads。</span><span class="sxs-lookup"><span data-stu-id="8f7fa-113">The second command sets the $CredsPath variable to C:\Downloads.</span></span>

<span data-ttu-id="8f7fa-114">最後一個命令會使用 Azure 備份 $CredsPath 中的認證來取得 $Vault 01 的保存庫認證檔案。</span><span class="sxs-lookup"><span data-stu-id="8f7fa-114">The last command gets the vault credentials file for $Vault01 using the credentials in $CredsPath for Azure Backup.</span></span>

## <span data-ttu-id="8f7fa-115">參數</span><span class="sxs-lookup"><span data-stu-id="8f7fa-115">PARAMETERS</span></span>

### <span data-ttu-id="8f7fa-116">-備份</span><span class="sxs-lookup"><span data-stu-id="8f7fa-116">-Backup</span></span>
<span data-ttu-id="8f7fa-117">表示保存庫認證檔案適用于 Azure 備份。</span><span class="sxs-lookup"><span data-stu-id="8f7fa-117">Indicates the vault credentials file is applicable to Azure Backup.</span></span>

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

### <span data-ttu-id="8f7fa-118">-Path</span><span class="sxs-lookup"><span data-stu-id="8f7fa-118">-Path</span></span>
<span data-ttu-id="8f7fa-119">指定 Azure Site Recovery 保存庫設定檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="8f7fa-119">Specifies the path to the Azure Site Recovery vault settings file.</span></span>
<span data-ttu-id="8f7fa-120">您可以從 Azure Site Recovery 保存庫入口網站下載此檔案，並將它儲存在本機。</span><span class="sxs-lookup"><span data-stu-id="8f7fa-120">You can download this file from the Azure Site Recovery vault portal and store it locally.</span></span>

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

### <span data-ttu-id="8f7fa-121">-SiteFriendlyName</span><span class="sxs-lookup"><span data-stu-id="8f7fa-121">-SiteFriendlyName</span></span>
<span data-ttu-id="8f7fa-122">指定網站的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="8f7fa-122">Specifies the site friendly name.</span></span>
<span data-ttu-id="8f7fa-123">如果您要下載 Hyper-v 網站的保存庫認證，請使用此參數。</span><span class="sxs-lookup"><span data-stu-id="8f7fa-123">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

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

### <span data-ttu-id="8f7fa-124">-SiteIdentifier</span><span class="sxs-lookup"><span data-stu-id="8f7fa-124">-SiteIdentifier</span></span>
<span data-ttu-id="8f7fa-125">指定網站識別碼。</span><span class="sxs-lookup"><span data-stu-id="8f7fa-125">Specifies the site identifier.</span></span>
<span data-ttu-id="8f7fa-126">如果您要下載 Hyper-v 網站的保存庫認證，請使用此參數。</span><span class="sxs-lookup"><span data-stu-id="8f7fa-126">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

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

### <span data-ttu-id="8f7fa-127">-SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="8f7fa-127">-SiteRecovery</span></span>
<span data-ttu-id="8f7fa-128">表示保存庫認證檔案適用于 Azure Site Recovery。</span><span class="sxs-lookup"><span data-stu-id="8f7fa-128">Indicates the vault credentials file is applicable to Azure Site Recovery.</span></span>

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

### <span data-ttu-id="8f7fa-129">-保存庫</span><span class="sxs-lookup"><span data-stu-id="8f7fa-129">-Vault</span></span>
<span data-ttu-id="8f7fa-130">指定 Azure Site Recovery 保存庫物件。</span><span class="sxs-lookup"><span data-stu-id="8f7fa-130">Specifies the Azure Site Recovery vault object.</span></span>

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

### <span data-ttu-id="8f7fa-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f7fa-131">-DefaultProfile</span></span>
<span data-ttu-id="8f7fa-132">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8f7fa-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f7fa-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f7fa-133">CommonParameters</span></span>
<span data-ttu-id="8f7fa-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8f7fa-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f7fa-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8f7fa-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f7fa-136">輸入</span><span class="sxs-lookup"><span data-stu-id="8f7fa-136">INPUTS</span></span>

### <span data-ttu-id="8f7fa-137">ARSVault</span><span class="sxs-lookup"><span data-stu-id="8f7fa-137">ARSVault</span></span>
<span data-ttu-id="8f7fa-138">參數 "Vault" 接受來自管線的 "ARSVault" 類型值</span><span class="sxs-lookup"><span data-stu-id="8f7fa-138">Parameter 'Vault' accepts value of type 'ARSVault' from the pipeline</span></span>

## <span data-ttu-id="8f7fa-139">輸出</span><span class="sxs-lookup"><span data-stu-id="8f7fa-139">OUTPUTS</span></span>

### <span data-ttu-id="8f7fa-140">VaultSettingsFilePath 中的 RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8f7fa-140">Microsoft.Azure.Commands.RecoveryServices.VaultSettingsFilePath</span></span>

## <span data-ttu-id="8f7fa-141">筆記</span><span class="sxs-lookup"><span data-stu-id="8f7fa-141">NOTES</span></span>

## <span data-ttu-id="8f7fa-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="8f7fa-142">RELATED LINKS</span></span>

[<span data-ttu-id="8f7fa-143">AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="8f7fa-143">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="8f7fa-144">新-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="8f7fa-144">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="8f7fa-145">移除-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="8f7fa-145">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


