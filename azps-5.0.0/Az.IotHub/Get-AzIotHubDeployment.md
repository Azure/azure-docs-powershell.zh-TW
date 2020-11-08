---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeployment.md
ms.openlocfilehash: 1440b77d753a27b1c2a7176be5b44ef69fca2e50
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139202"
---
# <span data-ttu-id="4f82b-101">Get-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="4f82b-101">Get-AzIotHubDeployment</span></span>

## <span data-ttu-id="4f82b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4f82b-102">SYNOPSIS</span></span>
<span data-ttu-id="4f82b-103">列出所有或特定的 IoT 邊緣部署。</span><span class="sxs-lookup"><span data-stu-id="4f82b-103">Lists all or a particular IoT Edge deployment.</span></span>

## <span data-ttu-id="4f82b-104">句法</span><span class="sxs-lookup"><span data-stu-id="4f82b-104">SYNTAX</span></span>

### <span data-ttu-id="4f82b-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="4f82b-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f82b-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4f82b-106">InputObjectSet</span></span>
```
Get-AzIotHubDeployment [-InputObject] <PSIotHub> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4f82b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4f82b-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeployment [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4f82b-108">說明</span><span class="sxs-lookup"><span data-stu-id="4f82b-108">DESCRIPTION</span></span>
<span data-ttu-id="4f82b-109">在 IoT 中樞中取得 IoT Edge 部署或清單 IoT Edge 部署的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="4f82b-109">Get the details of an IoT Edge deployment or List IoT Edge deployments in an IoT Hub.</span></span>
<span data-ttu-id="4f82b-110">如需詳細資訊，請參閱 https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring 。</span><span class="sxs-lookup"><span data-stu-id="4f82b-110">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring for more information.</span></span>

## <span data-ttu-id="4f82b-111">示例</span><span class="sxs-lookup"><span data-stu-id="4f82b-111">EXAMPLES</span></span>

### <span data-ttu-id="4f82b-112">範例1</span><span class="sxs-lookup"><span data-stu-id="4f82b-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1"
```

<span data-ttu-id="4f82b-113">取得 IoT Edge 部署的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="4f82b-113">Get the details of an IoT Edge deployment.</span></span>

### <span data-ttu-id="4f82b-114">範例2</span><span class="sxs-lookup"><span data-stu-id="4f82b-114">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="4f82b-115">列出 IoT 中樞中的所有 IoT Edge 部署。</span><span class="sxs-lookup"><span data-stu-id="4f82b-115">List all IoT Edge deployments in an IoT Hub.</span></span>

## <span data-ttu-id="4f82b-116">參數</span><span class="sxs-lookup"><span data-stu-id="4f82b-116">PARAMETERS</span></span>

### <span data-ttu-id="4f82b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f82b-117">-DefaultProfile</span></span>
<span data-ttu-id="4f82b-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4f82b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f82b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4f82b-119">-InputObject</span></span>
<span data-ttu-id="4f82b-120">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="4f82b-120">IotHub object</span></span>

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

### <span data-ttu-id="4f82b-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="4f82b-121">-IotHubName</span></span>
<span data-ttu-id="4f82b-122">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="4f82b-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="4f82b-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="4f82b-123">-Name</span></span>
<span data-ttu-id="4f82b-124">部署的識別碼。</span><span class="sxs-lookup"><span data-stu-id="4f82b-124">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="4f82b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f82b-125">-ResourceGroupName</span></span>
<span data-ttu-id="4f82b-126">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="4f82b-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="4f82b-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4f82b-127">-ResourceId</span></span>
<span data-ttu-id="4f82b-128">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="4f82b-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="4f82b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f82b-129">CommonParameters</span></span>
<span data-ttu-id="4f82b-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4f82b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f82b-131">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4f82b-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f82b-132">輸入</span><span class="sxs-lookup"><span data-stu-id="4f82b-132">INPUTS</span></span>

### <span data-ttu-id="4f82b-133">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="4f82b-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="4f82b-134">System.object</span><span class="sxs-lookup"><span data-stu-id="4f82b-134">System.String</span></span>

## <span data-ttu-id="4f82b-135">輸出</span><span class="sxs-lookup"><span data-stu-id="4f82b-135">OUTPUTS</span></span>

### <span data-ttu-id="4f82b-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="4f82b-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

### <span data-ttu-id="4f82b-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployments []</span><span class="sxs-lookup"><span data-stu-id="4f82b-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployments[]</span></span>

## <span data-ttu-id="4f82b-138">筆記</span><span class="sxs-lookup"><span data-stu-id="4f82b-138">NOTES</span></span>

## <span data-ttu-id="4f82b-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="4f82b-139">RELATED LINKS</span></span>