---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubmoduletwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleTwin.md
ms.openlocfilehash: 5a033bd0d43f614dd7fa1dd45cb3581d6808309d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959777"
---
# <span data-ttu-id="2b841-101">Get-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="2b841-101">Get-AzIotHubModuleTwin</span></span>

## <span data-ttu-id="2b841-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2b841-102">SYNOPSIS</span></span>
<span data-ttu-id="2b841-103">取得 IoT 裝置模組雙子出的模式。</span><span class="sxs-lookup"><span data-stu-id="2b841-103">Gets an IoT device module twin.</span></span>

## <span data-ttu-id="2b841-104">句法</span><span class="sxs-lookup"><span data-stu-id="2b841-104">SYNTAX</span></span>

### <span data-ttu-id="2b841-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="2b841-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubModuleTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 -ModuleId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b841-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2b841-106">InputObjectSet</span></span>
```
Get-AzIotHubModuleTwin [-InputObject] <PSIotHub> [-DeviceId] <String> -ModuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b841-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2b841-107">ResourceIdSet</span></span>
```
Get-AzIotHubModuleTwin [-ResourceId] <String> [-DeviceId] <String> -ModuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b841-108">說明</span><span class="sxs-lookup"><span data-stu-id="2b841-108">DESCRIPTION</span></span>
<span data-ttu-id="2b841-109">取得 IoT 裝置模組雙子出的模式。</span><span class="sxs-lookup"><span data-stu-id="2b841-109">Gets an IoT device module twin.</span></span> <span data-ttu-id="2b841-110">如需詳細資訊，請參閱 https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twins 。</span><span class="sxs-lookup"><span data-stu-id="2b841-110">See https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twins for more information.</span></span>

## <span data-ttu-id="2b841-111">示例</span><span class="sxs-lookup"><span data-stu-id="2b841-111">EXAMPLES</span></span>

### <span data-ttu-id="2b841-112">範例1</span><span class="sxs-lookup"><span data-stu-id="2b841-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1"
```

<span data-ttu-id="2b841-113">傳回 device module 雙子物件。</span><span class="sxs-lookup"><span data-stu-id="2b841-113">Returns the device module twin object.</span></span>

## <span data-ttu-id="2b841-114">參數</span><span class="sxs-lookup"><span data-stu-id="2b841-114">PARAMETERS</span></span>

### <span data-ttu-id="2b841-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b841-115">-DefaultProfile</span></span>
<span data-ttu-id="2b841-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2b841-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b841-117">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="2b841-117">-DeviceId</span></span>
<span data-ttu-id="2b841-118">目標裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="2b841-118">Target Device Id.</span></span>

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

### <span data-ttu-id="2b841-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2b841-119">-InputObject</span></span>
<span data-ttu-id="2b841-120">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="2b841-120">IotHub object</span></span>

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

### <span data-ttu-id="2b841-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="2b841-121">-IotHubName</span></span>
<span data-ttu-id="2b841-122">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="2b841-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="2b841-123">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="2b841-123">-ModuleId</span></span>
<span data-ttu-id="2b841-124">目的模組識別碼。</span><span class="sxs-lookup"><span data-stu-id="2b841-124">Target Module Id.</span></span>

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

### <span data-ttu-id="2b841-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b841-125">-ResourceGroupName</span></span>
<span data-ttu-id="2b841-126">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="2b841-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="2b841-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2b841-127">-ResourceId</span></span>
<span data-ttu-id="2b841-128">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="2b841-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="2b841-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b841-129">CommonParameters</span></span>
<span data-ttu-id="2b841-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2b841-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b841-131">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2b841-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b841-132">輸入</span><span class="sxs-lookup"><span data-stu-id="2b841-132">INPUTS</span></span>

### <span data-ttu-id="2b841-133">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="2b841-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="2b841-134">System.object</span><span class="sxs-lookup"><span data-stu-id="2b841-134">System.String</span></span>

## <span data-ttu-id="2b841-135">輸出</span><span class="sxs-lookup"><span data-stu-id="2b841-135">OUTPUTS</span></span>

### <span data-ttu-id="2b841-136">PSModuleTwin （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="2b841-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleTwin</span></span>

## <span data-ttu-id="2b841-137">筆記</span><span class="sxs-lookup"><span data-stu-id="2b841-137">NOTES</span></span>

## <span data-ttu-id="2b841-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="2b841-138">RELATED LINKS</span></span>
