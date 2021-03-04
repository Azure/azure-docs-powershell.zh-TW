---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConfiguration.md
ms.openlocfilehash: b50d0b493243a07632403890d0324fefaba7dc8c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911086"
---
# <span data-ttu-id="b269d-101">Get-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="b269d-101">Get-AzIotHubConfiguration</span></span>

## <span data-ttu-id="b269d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b269d-102">SYNOPSIS</span></span>
<span data-ttu-id="b269d-103">列出所有或特定的 IoT 自動裝置管理組式。</span><span class="sxs-lookup"><span data-stu-id="b269d-103">Lists all or a particular IoT automatic device management configuration.</span></span>

## <span data-ttu-id="b269d-104">語法</span><span class="sxs-lookup"><span data-stu-id="b269d-104">SYNTAX</span></span>

### <span data-ttu-id="b269d-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b269d-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b269d-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b269d-106">InputObjectSet</span></span>
```
Get-AzIotHubConfiguration [-InputObject] <PSIotHub> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b269d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b269d-107">ResourceIdSet</span></span>
```
Get-AzIotHubConfiguration [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b269d-108">描述</span><span class="sxs-lookup"><span data-stu-id="b269d-108">DESCRIPTION</span></span>
<span data-ttu-id="b269d-109">取得 IoT 自動裝置管理組配置的詳細資訊，或列出 IoT 中心中的 IoT 自動裝置管理群組原則。</span><span class="sxs-lookup"><span data-stu-id="b269d-109">Get the details of an IoT automatic device management configuration or list IoT automatic device management configurations in an IoT Hub.</span></span>
<span data-ttu-id="b269d-110">請參閱 https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management 詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="b269d-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="b269d-111">例子</span><span class="sxs-lookup"><span data-stu-id="b269d-111">EXAMPLES</span></span>

### <span data-ttu-id="b269d-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="b269d-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1"
```

<span data-ttu-id="b269d-113">取得 IoT 自動裝置管理組配置的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="b269d-113">Get the details of an IoT automatic device management configuration.</span></span>

### <span data-ttu-id="b269d-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="b269d-114">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="b269d-115">列出 IoT 中心中的 IoT 自動裝置管理群組原則。</span><span class="sxs-lookup"><span data-stu-id="b269d-115">List IoT automatic device management configurations in an IoT Hub.</span></span>

## <span data-ttu-id="b269d-116">參數</span><span class="sxs-lookup"><span data-stu-id="b269d-116">PARAMETERS</span></span>

### <span data-ttu-id="b269d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b269d-117">-DefaultProfile</span></span>
<span data-ttu-id="b269d-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b269d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b269d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b269d-119">-InputObject</span></span>
<span data-ttu-id="b269d-120">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="b269d-120">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b269d-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="b269d-121">-IotHubName</span></span>
<span data-ttu-id="b269d-122">Iot Hub 的名稱</span><span class="sxs-lookup"><span data-stu-id="b269d-122">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b269d-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="b269d-123">-Name</span></span>
<span data-ttu-id="b269d-124">組配置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b269d-124">Identifier for the configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b269d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b269d-125">-ResourceGroupName</span></span>
<span data-ttu-id="b269d-126">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="b269d-126">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b269d-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b269d-127">-ResourceId</span></span>
<span data-ttu-id="b269d-128">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="b269d-128">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b269d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b269d-129">CommonParameters</span></span>
<span data-ttu-id="b269d-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b269d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b269d-131">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="b269d-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b269d-132">輸入</span><span class="sxs-lookup"><span data-stu-id="b269d-132">INPUTS</span></span>

### <span data-ttu-id="b269d-133">Microsoft.Azure.Commands.management.IotHub.models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="b269d-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="b269d-134">System.String</span><span class="sxs-lookup"><span data-stu-id="b269d-134">System.String</span></span>

## <span data-ttu-id="b269d-135">輸出</span><span class="sxs-lookup"><span data-stu-id="b269d-135">OUTPUTS</span></span>

### <span data-ttu-id="b269d-136">Microsoft.Azure.Commands.management.IotHub.models.PSConfiguration</span><span class="sxs-lookup"><span data-stu-id="b269d-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span></span>

### <span data-ttu-id="b269d-137">Microsoft.Azure.Commands.management.IotHub.models.PSConfigurations[]</span><span class="sxs-lookup"><span data-stu-id="b269d-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurations[]</span></span>

## <span data-ttu-id="b269d-138">筆記</span><span class="sxs-lookup"><span data-stu-id="b269d-138">NOTES</span></span>

## <span data-ttu-id="b269d-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="b269d-139">RELATED LINKS</span></span>
