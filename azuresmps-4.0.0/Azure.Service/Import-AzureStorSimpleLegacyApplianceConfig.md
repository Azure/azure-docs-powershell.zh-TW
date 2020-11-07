---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F41E3B17-A33C-4FBF-B532-2E86F1AAE2B8
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf4bc3e4245e3d223d95c3ec5d793a53d5d3bfbe
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967705"
---
# <span data-ttu-id="b128e-101">Import-AzureStorSimpleLegacyApplianceConfig</span><span class="sxs-lookup"><span data-stu-id="b128e-101">Import-AzureStorSimpleLegacyApplianceConfig</span></span>

## <span data-ttu-id="b128e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b128e-102">SYNOPSIS</span></span>
<span data-ttu-id="b128e-103">匯入設定檔。</span><span class="sxs-lookup"><span data-stu-id="b128e-103">Imports a configuration file.</span></span>

## <span data-ttu-id="b128e-104">句法</span><span class="sxs-lookup"><span data-stu-id="b128e-104">SYNTAX</span></span>

```
Import-AzureStorSimpleLegacyApplianceConfig -ConfigFilePath <String> -TargetDeviceName <String>
 -ConfigDecryptionKey <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b128e-105">說明</span><span class="sxs-lookup"><span data-stu-id="b128e-105">DESCRIPTION</span></span>
<span data-ttu-id="b128e-106">匯 **入-AzureStorSimpleLegacyApplianceConfig** Cmdlet 會從舊版裝置中匯入設定檔。</span><span class="sxs-lookup"><span data-stu-id="b128e-106">The **Import-AzureStorSimpleLegacyApplianceConfig** cmdlet imports the configuration file from the legacy appliance.</span></span>
<span data-ttu-id="b128e-107">該檔案包含 Azure StorSimple service 的大量容器、備份原則及儲存帳號憑證的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b128e-107">That file contains information about volume containers, backup policies, and storage account credentials for the Azure StorSimple service.</span></span>
<span data-ttu-id="b128e-108">這個 Cmdlet 會傳回舊版裝置配置中繼資料。</span><span class="sxs-lookup"><span data-stu-id="b128e-108">This cmdlet returns the legacy appliance configuration metadata.</span></span>

## <span data-ttu-id="b128e-109">示例</span><span class="sxs-lookup"><span data-stu-id="b128e-109">EXAMPLES</span></span>

### <span data-ttu-id="b128e-110">範例1：匯入設定檔</span><span class="sxs-lookup"><span data-stu-id="b128e-110">Example 1: Import a configuration file</span></span>
```
PS C:\>Import-AzureStorSimpleLegacyApplianceConfig -ConfigFilePath "C:\MigrationData\LegacyStorSimpleConfig.sse" -TargetDeviceName "8100-123456789" -ConfigDecryptionKey "fWs793hHVhR90NKdDYTeNq"
LegacyConfigId      : e2d5c9b1-b528-4c21-b8ae-533feefc8a41
ImportedOn          : 4/8/2015 7:23:04 PM
ConfigFile          : D:\configs\StorSimpleConfig_27_Mar_15_12_19.xml.sse
TargetApplianceName : Arunkm-N4
Details             : Available Cloud Configuration(s) for migration : 
                          Cloud Configuration(s) 1    : TC8Cloud[Stingray19-FP6] 
                          Cloud Configuration(s) 2    : fulle_cc4
                          Cloud Configuration(s) 3    : fulle_cc2
                          Cloud Configuration(s) 4    : fulle_cc3
                          Cloud Configuration(s) 5    : TC9Cloud[Stingray18-FP3] 
                          Cloud Configuration(s) 6    : fulle_cc1
                          Cloud Configuration(s) 7    : Container-New[Stingray19-FP6] 
                          Cloud Configuration(s) 8    : TC6Cloud[Stingray19-FP6] 
                          Cloud Configuration(s) 9    : TC7Cloud[Stingray18-FP3] 

Result              : Successfully imported config from the legacy appliance! 
Save the legacy config id and cloud configuration(s) for future reference.
```

<span data-ttu-id="b128e-111">這個命令會在指定的路徑中匯入配置檔案。</span><span class="sxs-lookup"><span data-stu-id="b128e-111">This command imports the configuration file at the specified path.</span></span>
<span data-ttu-id="b128e-112">此命令包含用來解密檔案的金鑰。</span><span class="sxs-lookup"><span data-stu-id="b128e-112">The command includes the key to decrypt the file.</span></span>

## <span data-ttu-id="b128e-113">參數</span><span class="sxs-lookup"><span data-stu-id="b128e-113">PARAMETERS</span></span>

### <span data-ttu-id="b128e-114">-ConfigDecryptionKey</span><span class="sxs-lookup"><span data-stu-id="b128e-114">-ConfigDecryptionKey</span></span>
<span data-ttu-id="b128e-115">指定舊版裝置的 [解密金鑰]。</span><span class="sxs-lookup"><span data-stu-id="b128e-115">Specifies the decryption key for the configuration of the legacy appliance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b128e-116">-ConfigFilePath</span><span class="sxs-lookup"><span data-stu-id="b128e-116">-ConfigFilePath</span></span>
<span data-ttu-id="b128e-117">指定要取得的設定檔的絕對路徑。</span><span class="sxs-lookup"><span data-stu-id="b128e-117">Specifies the absolute path of the configuration file to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: FilePath

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b128e-118">-設定檔</span><span class="sxs-lookup"><span data-stu-id="b128e-118">-Profile</span></span>
<span data-ttu-id="b128e-119">指定 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="b128e-119">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="b128e-120">-TargetDeviceName</span><span class="sxs-lookup"><span data-stu-id="b128e-120">-TargetDeviceName</span></span>
<span data-ttu-id="b128e-121">指定入口網站中所呈現之目標裝置的名稱。</span><span class="sxs-lookup"><span data-stu-id="b128e-121">Specifies the name of the target device as presented in the portal.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b128e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b128e-122">CommonParameters</span></span>
<span data-ttu-id="b128e-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b128e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b128e-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b128e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b128e-125">輸入</span><span class="sxs-lookup"><span data-stu-id="b128e-125">INPUTS</span></span>

### <span data-ttu-id="b128e-126">所有</span><span class="sxs-lookup"><span data-stu-id="b128e-126">None</span></span>

## <span data-ttu-id="b128e-127">輸出</span><span class="sxs-lookup"><span data-stu-id="b128e-127">OUTPUTS</span></span>

### <span data-ttu-id="b128e-128">LegacyApplianceConfiguration</span><span class="sxs-lookup"><span data-stu-id="b128e-128">LegacyApplianceConfiguration</span></span>
<span data-ttu-id="b128e-129">這個 Cmdlet 會傳回配置的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="b128e-129">This cmdlet returns the details of the configuration.</span></span>
<span data-ttu-id="b128e-130">**LegacyApplianceConfiguration** 物件包含下列資訊：配置識別碼、卷容器名稱、存取控制記錄、備份原則、頻寬設定、卷容器、儲存帳號憑證及卷名。</span><span class="sxs-lookup"><span data-stu-id="b128e-130">The **LegacyApplianceConfiguration** object contains the following information: configuration ID, volume container names, access control records, backup policies, bandwidth settings, volume containers, storage account credentials, and volumes.</span></span>

## <span data-ttu-id="b128e-131">筆記</span><span class="sxs-lookup"><span data-stu-id="b128e-131">NOTES</span></span>

## <span data-ttu-id="b128e-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="b128e-132">RELATED LINKS</span></span>

[<span data-ttu-id="b128e-133">匯入-AzureStorSimpleLegacyVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="b128e-133">Import-AzureStorSimpleLegacyVolumeContainer</span></span>](./Import-AzureStorSimpleLegacyVolumeContainer.md)


