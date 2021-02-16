---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/new-azcloudservicediagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceDiagnosticsExtension.md
ms.openlocfilehash: 96651a495f08657a4cd9006545cfa104285ec7ed
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100139386"
---
# <span data-ttu-id="61a0a-101">New-AzCloudServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="61a0a-101">New-AzCloudServiceDiagnosticsExtension</span></span>

## <span data-ttu-id="61a0a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="61a0a-102">SYNOPSIS</span></span>
<span data-ttu-id="61a0a-103">在記憶體中建立診斷延伸的物件</span><span class="sxs-lookup"><span data-stu-id="61a0a-103">Create a in-memory object for Diagnostics Extension</span></span>

## <span data-ttu-id="61a0a-104">句法</span><span class="sxs-lookup"><span data-stu-id="61a0a-104">SYNTAX</span></span>

```
New-AzCloudServiceDiagnosticsExtension [-Name] <String> [-ResourceGroupName] <String>
 [-CloudServiceName] <String> [-DiagnosticsConfigurationPath] <String> [-StorageAccountName] <String>
 [-StorageAccountKey] <String> [[-Subscription] <String>] [[-TypeHandlerVersion] <String>]
 [[-RolesAppliedTo] <String[]>] [[-AutoUpgradeMinorVersion] <Boolean>] [<CommonParameters>]
```

## <span data-ttu-id="61a0a-105">說明</span><span class="sxs-lookup"><span data-stu-id="61a0a-105">DESCRIPTION</span></span>
<span data-ttu-id="61a0a-106">在記憶體中建立診斷延伸的物件</span><span class="sxs-lookup"><span data-stu-id="61a0a-106">Create a in-memory object for Diagnostics Extension</span></span>

## <span data-ttu-id="61a0a-107">示例</span><span class="sxs-lookup"><span data-stu-id="61a0a-107">EXAMPLES</span></span>

### <span data-ttu-id="61a0a-108">範例1：建立診斷延伸物件</span><span class="sxs-lookup"><span data-stu-id="61a0a-108">Example 1: Create diagnostics extension object</span></span>
```powershell
PS C:\> $storageAccountKey = Get-AzStorageAccountKey -ResourceGroupName "ContosOrg" -Name "ContosSA"
PS C:\> $configFile = "<WAD configuration file path>"
PS C:\> $extension = New-AzCloudServiceDiagnosticsExtension -Name "WADExtension" -ResourceGroupName "ContosOrg" -CloudServiceName "ContosCS" -StorageAccountName "ContosSA" -StorageAccountKey $storageAccountKey[0].Value -DiagnosticsConfigurationPath $configFile -TypeHandlerVersion "1.5" -AutoUpgradeMinorVersion $true
```

<span data-ttu-id="61a0a-109">這個命令會建立用來建立或更新雲端服務的診斷延伸物件。</span><span class="sxs-lookup"><span data-stu-id="61a0a-109">This command creates diagnostics extension object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="61a0a-110">如需詳細資訊，請參閱新 AzCloudService。</span><span class="sxs-lookup"><span data-stu-id="61a0a-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="61a0a-111">參數</span><span class="sxs-lookup"><span data-stu-id="61a0a-111">PARAMETERS</span></span>

### <span data-ttu-id="61a0a-112">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="61a0a-112">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="61a0a-113">自動升級次要版本。</span><span class="sxs-lookup"><span data-stu-id="61a0a-113">Auto upgrade minor version.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61a0a-114">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="61a0a-114">-CloudServiceName</span></span>
<span data-ttu-id="61a0a-115">雲端服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="61a0a-115">Name of Cloud Service.</span></span>

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

### <span data-ttu-id="61a0a-116">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="61a0a-116">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="61a0a-117">指定 Azure 診斷的配置。</span><span class="sxs-lookup"><span data-stu-id="61a0a-117">Specifies the configuration for Azure Diagnostics.</span></span>
<span data-ttu-id="61a0a-118">您可以使用下列命令來下載架構： (AzureServiceAvailableExtension-ExtensionName ' PaaSDiagnostics」-ProviderNamespace "" ) 。PublicConfigurationSchema |Out-File 編碼 utf8-FilePath ' WadConfig</span><span class="sxs-lookup"><span data-stu-id="61a0a-118">You can download the schema by using the following command: (Get-AzureServiceAvailableExtension -ExtensionName 'PaaSDiagnostics' -ProviderNamespace 'Microsoft.Azure.Diagnostics').PublicConfigurationSchema | Out-File -Encoding utf8 -FilePath 'WadConfig.xsd'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61a0a-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="61a0a-119">-Name</span></span>
<span data-ttu-id="61a0a-120">診斷延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="61a0a-120">Name of Diagnostics Extension.</span></span>

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

### <span data-ttu-id="61a0a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61a0a-121">-ResourceGroupName</span></span>
<span data-ttu-id="61a0a-122">雲端服務的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="61a0a-122">Resource Group name of Cloud Service.</span></span>

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

### <span data-ttu-id="61a0a-123">-RolesAppliedTo</span><span class="sxs-lookup"><span data-stu-id="61a0a-123">-RolesAppliedTo</span></span>
<span data-ttu-id="61a0a-124">已套用的角色。</span><span class="sxs-lookup"><span data-stu-id="61a0a-124">Roles applied to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61a0a-125">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="61a0a-125">-StorageAccountKey</span></span>
<span data-ttu-id="61a0a-126">儲存空間帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="61a0a-126">Storage Account Key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61a0a-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="61a0a-127">-StorageAccountName</span></span>
<span data-ttu-id="61a0a-128">儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="61a0a-128">Name of the Storage Account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61a0a-129">-訂閱</span><span class="sxs-lookup"><span data-stu-id="61a0a-129">-Subscription</span></span>
<span data-ttu-id="61a0a-130">訂閱.</span><span class="sxs-lookup"><span data-stu-id="61a0a-130">Subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61a0a-131">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="61a0a-131">-TypeHandlerVersion</span></span>
<span data-ttu-id="61a0a-132">指定副檔名的版本。</span><span class="sxs-lookup"><span data-stu-id="61a0a-132">Specifies the version of the extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61a0a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61a0a-133">CommonParameters</span></span>
<span data-ttu-id="61a0a-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="61a0a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61a0a-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="61a0a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61a0a-136">輸入</span><span class="sxs-lookup"><span data-stu-id="61a0a-136">INPUTS</span></span>

## <span data-ttu-id="61a0a-137">輸出</span><span class="sxs-lookup"><span data-stu-id="61a0a-137">OUTPUTS</span></span>

### <span data-ttu-id="61a0a-138">Api20201001Preview. CloudService...。</span><span class="sxs-lookup"><span data-stu-id="61a0a-138">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span></span>

## <span data-ttu-id="61a0a-139">筆記</span><span class="sxs-lookup"><span data-stu-id="61a0a-139">NOTES</span></span>

<span data-ttu-id="61a0a-140">別名</span><span class="sxs-lookup"><span data-stu-id="61a0a-140">ALIASES</span></span>

## <span data-ttu-id="61a0a-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="61a0a-141">RELATED LINKS</span></span>

