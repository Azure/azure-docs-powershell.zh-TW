---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/new-azcloudservicediagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceDiagnosticsExtension.md
ms.openlocfilehash: a87e9c76b2c083392fc37d74a3ba213dba5881ee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906325"
---
# <span data-ttu-id="b907c-101">New-AzCloudServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="b907c-101">New-AzCloudServiceDiagnosticsExtension</span></span>

## <span data-ttu-id="b907c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b907c-102">SYNOPSIS</span></span>
<span data-ttu-id="b907c-103">為診斷擴充功能建立記憶體內物件</span><span class="sxs-lookup"><span data-stu-id="b907c-103">Create a in-memory object for Diagnostics Extension</span></span>

## <span data-ttu-id="b907c-104">語法</span><span class="sxs-lookup"><span data-stu-id="b907c-104">SYNTAX</span></span>

```
New-AzCloudServiceDiagnosticsExtension [-Name] <String> [-ResourceGroupName] <String>
 [-CloudServiceName] <String> [-DiagnosticsConfigurationPath] <String> [-StorageAccountName] <String>
 [-StorageAccountKey] <String> [[-Subscription] <String>] [[-TypeHandlerVersion] <String>]
 [[-RolesAppliedTo] <String[]>] [[-AutoUpgradeMinorVersion] <Boolean>] [<CommonParameters>]
```

## <span data-ttu-id="b907c-105">描述</span><span class="sxs-lookup"><span data-stu-id="b907c-105">DESCRIPTION</span></span>
<span data-ttu-id="b907c-106">為診斷擴充功能建立記憶體內物件</span><span class="sxs-lookup"><span data-stu-id="b907c-106">Create a in-memory object for Diagnostics Extension</span></span>

## <span data-ttu-id="b907c-107">例子</span><span class="sxs-lookup"><span data-stu-id="b907c-107">EXAMPLES</span></span>

### <span data-ttu-id="b907c-108">範例 1：建立診斷擴充物件</span><span class="sxs-lookup"><span data-stu-id="b907c-108">Example 1: Create diagnostics extension object</span></span>
```powershell
PS C:\> $storageAccountKey = Get-AzStorageAccountKey -ResourceGroupName "ContosOrg" -Name "ContosSA"
PS C:\> $configFile = "<WAD configuration file path>"
PS C:\> $extension = New-AzCloudServiceDiagnosticsExtension -Name "WADExtension" -ResourceGroupName "ContosOrg" -CloudServiceName "ContosCS" -StorageAccountName "ContosSA" -StorageAccountKey $storageAccountKey[0].Value -DiagnosticsConfigurationPath $configFile -TypeHandlerVersion "1.5" -AutoUpgradeMinorVersion $true
```

<span data-ttu-id="b907c-109">此命令會建立診斷擴充物件，用於建立或更新雲端服務。</span><span class="sxs-lookup"><span data-stu-id="b907c-109">This command creates diagnostics extension object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="b907c-110">詳情請參閱 New-AzCloudService。</span><span class="sxs-lookup"><span data-stu-id="b907c-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="b907c-111">參數</span><span class="sxs-lookup"><span data-stu-id="b907c-111">PARAMETERS</span></span>

### <span data-ttu-id="b907c-112">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="b907c-112">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="b907c-113">自動升級次要版本。</span><span class="sxs-lookup"><span data-stu-id="b907c-113">Auto upgrade minor version.</span></span>

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

### <span data-ttu-id="b907c-114">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="b907c-114">-CloudServiceName</span></span>
<span data-ttu-id="b907c-115">雲端服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="b907c-115">Name of Cloud Service.</span></span>

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

### <span data-ttu-id="b907c-116">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="b907c-116">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="b907c-117">指定 Azure 診斷的群組原則。</span><span class="sxs-lookup"><span data-stu-id="b907c-117">Specifies the configuration for Azure Diagnostics.</span></span>
<span data-ttu-id="b907c-118">您可以使用下列命令下載架構： (Get-AzureServiceAvailableExtension -ExtensionName 'PaaSDiagnostics' -ProviderNamespace 'Microsoft.Azure.Diagnostics') 。PublicConfigurationSchema |Out-File編碼 utf8 -FilePath 'WadConfig.xsd'</span><span class="sxs-lookup"><span data-stu-id="b907c-118">You can download the schema by using the following command: (Get-AzureServiceAvailableExtension -ExtensionName 'PaaSDiagnostics' -ProviderNamespace 'Microsoft.Azure.Diagnostics').PublicConfigurationSchema | Out-File -Encoding utf8 -FilePath 'WadConfig.xsd'</span></span>

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

### <span data-ttu-id="b907c-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="b907c-119">-Name</span></span>
<span data-ttu-id="b907c-120">診斷擴充功能的名稱。</span><span class="sxs-lookup"><span data-stu-id="b907c-120">Name of Diagnostics Extension.</span></span>

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

### <span data-ttu-id="b907c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b907c-121">-ResourceGroupName</span></span>
<span data-ttu-id="b907c-122">雲端服務的資源組名。</span><span class="sxs-lookup"><span data-stu-id="b907c-122">Resource Group name of Cloud Service.</span></span>

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

### <span data-ttu-id="b907c-123">-RolesAppliedTo</span><span class="sxs-lookup"><span data-stu-id="b907c-123">-RolesAppliedTo</span></span>
<span data-ttu-id="b907c-124">角色。</span><span class="sxs-lookup"><span data-stu-id="b907c-124">Roles applied to.</span></span>

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

### <span data-ttu-id="b907c-125">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="b907c-125">-StorageAccountKey</span></span>
<span data-ttu-id="b907c-126">儲存空間帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="b907c-126">Storage Account Key.</span></span>

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

### <span data-ttu-id="b907c-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b907c-127">-StorageAccountName</span></span>
<span data-ttu-id="b907c-128">儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="b907c-128">Name of the Storage Account.</span></span>

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

### <span data-ttu-id="b907c-129">-訂閱</span><span class="sxs-lookup"><span data-stu-id="b907c-129">-Subscription</span></span>
<span data-ttu-id="b907c-130">訂閱。</span><span class="sxs-lookup"><span data-stu-id="b907c-130">Subscription.</span></span>

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

### <span data-ttu-id="b907c-131">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="b907c-131">-TypeHandlerVersion</span></span>
<span data-ttu-id="b907c-132">指定擴充功能的版本。</span><span class="sxs-lookup"><span data-stu-id="b907c-132">Specifies the version of the extension.</span></span>

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

### <span data-ttu-id="b907c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b907c-133">CommonParameters</span></span>
<span data-ttu-id="b907c-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b907c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b907c-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b907c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b907c-136">輸入</span><span class="sxs-lookup"><span data-stu-id="b907c-136">INPUTS</span></span>

## <span data-ttu-id="b907c-137">輸出</span><span class="sxs-lookup"><span data-stu-id="b907c-137">OUTPUTS</span></span>

### <span data-ttu-id="b907c-138">Microsoft.Azure.PowerShell.Cmdlets.CloudService.models.Api20201001Preview.extension</span><span class="sxs-lookup"><span data-stu-id="b907c-138">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span></span>

## <span data-ttu-id="b907c-139">筆記</span><span class="sxs-lookup"><span data-stu-id="b907c-139">NOTES</span></span>

<span data-ttu-id="b907c-140">別名</span><span class="sxs-lookup"><span data-stu-id="b907c-140">ALIASES</span></span>

## <span data-ttu-id="b907c-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="b907c-141">RELATED LINKS</span></span>

