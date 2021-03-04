---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubmoduletwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleTwin.md
ms.openlocfilehash: 915fdf5bd0e53e7e8ed2817d83438597d515007d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911033"
---
# <span data-ttu-id="2c7a9-101">Get-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="2c7a9-101">Get-AzIotHubModuleTwin</span></span>

## <span data-ttu-id="2c7a9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2c7a9-102">SYNOPSIS</span></span>
<span data-ttu-id="2c7a9-103">獲得 IoT 裝置模組介面。</span><span class="sxs-lookup"><span data-stu-id="2c7a9-103">Gets an IoT device module twin.</span></span>

## <span data-ttu-id="2c7a9-104">語法</span><span class="sxs-lookup"><span data-stu-id="2c7a9-104">SYNTAX</span></span>

### <span data-ttu-id="2c7a9-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="2c7a9-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubModuleTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 -ModuleId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c7a9-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2c7a9-106">InputObjectSet</span></span>
```
Get-AzIotHubModuleTwin [-InputObject] <PSIotHub> [-DeviceId] <String> -ModuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c7a9-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2c7a9-107">ResourceIdSet</span></span>
```
Get-AzIotHubModuleTwin [-ResourceId] <String> [-DeviceId] <String> -ModuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c7a9-108">描述</span><span class="sxs-lookup"><span data-stu-id="2c7a9-108">DESCRIPTION</span></span>
<span data-ttu-id="2c7a9-109">獲得 IoT 裝置模組介面。</span><span class="sxs-lookup"><span data-stu-id="2c7a9-109">Gets an IoT device module twin.</span></span> <span data-ttu-id="2c7a9-110">請參閱 https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-module-twins 詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="2c7a9-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-module-twins for more information.</span></span>

## <span data-ttu-id="2c7a9-111">例子</span><span class="sxs-lookup"><span data-stu-id="2c7a9-111">EXAMPLES</span></span>

### <span data-ttu-id="2c7a9-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="2c7a9-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1"
```

<span data-ttu-id="2c7a9-113">會返回裝置模組物件。</span><span class="sxs-lookup"><span data-stu-id="2c7a9-113">Returns the device module twin object.</span></span>

## <span data-ttu-id="2c7a9-114">參數</span><span class="sxs-lookup"><span data-stu-id="2c7a9-114">PARAMETERS</span></span>

### <span data-ttu-id="2c7a9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c7a9-115">-DefaultProfile</span></span>
<span data-ttu-id="2c7a9-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2c7a9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c7a9-117">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="2c7a9-117">-DeviceId</span></span>
<span data-ttu-id="2c7a9-118">目標裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="2c7a9-118">Target Device Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c7a9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2c7a9-119">-InputObject</span></span>
<span data-ttu-id="2c7a9-120">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="2c7a9-120">IotHub object</span></span>

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

### <span data-ttu-id="2c7a9-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="2c7a9-121">-IotHubName</span></span>
<span data-ttu-id="2c7a9-122">Iot Hub 的名稱</span><span class="sxs-lookup"><span data-stu-id="2c7a9-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="2c7a9-123">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="2c7a9-123">-ModuleId</span></span>
<span data-ttu-id="2c7a9-124">目的模組識別碼。</span><span class="sxs-lookup"><span data-stu-id="2c7a9-124">Target Module Id.</span></span>

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

### <span data-ttu-id="2c7a9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c7a9-125">-ResourceGroupName</span></span>
<span data-ttu-id="2c7a9-126">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="2c7a9-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="2c7a9-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2c7a9-127">-ResourceId</span></span>
<span data-ttu-id="2c7a9-128">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="2c7a9-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="2c7a9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c7a9-129">CommonParameters</span></span>
<span data-ttu-id="2c7a9-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2c7a9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c7a9-131">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="2c7a9-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c7a9-132">輸入</span><span class="sxs-lookup"><span data-stu-id="2c7a9-132">INPUTS</span></span>

### <span data-ttu-id="2c7a9-133">Microsoft.Azure.Commands.management.IotHub.models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="2c7a9-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="2c7a9-134">System.String</span><span class="sxs-lookup"><span data-stu-id="2c7a9-134">System.String</span></span>

## <span data-ttu-id="2c7a9-135">輸出</span><span class="sxs-lookup"><span data-stu-id="2c7a9-135">OUTPUTS</span></span>

### <span data-ttu-id="2c7a9-136">Microsoft.Azure.Commands.management.IotHub.models.PSModuleTwin</span><span class="sxs-lookup"><span data-stu-id="2c7a9-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleTwin</span></span>

## <span data-ttu-id="2c7a9-137">筆記</span><span class="sxs-lookup"><span data-stu-id="2c7a9-137">NOTES</span></span>

## <span data-ttu-id="2c7a9-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="2c7a9-138">RELATED LINKS</span></span>
