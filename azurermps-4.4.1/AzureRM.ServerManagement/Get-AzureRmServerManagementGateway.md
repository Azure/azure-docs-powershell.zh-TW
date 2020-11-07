---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: C579BF90-FD8B-4384-96EB-46154E308492
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementGateway.md
ms.openlocfilehash: 6b98f4266e730e1cfb60ef51046e6846f24999d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624137"
---
# <span data-ttu-id="60ece-101">Get-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="60ece-101">Get-AzureRmServerManagementGateway</span></span>

## <span data-ttu-id="60ece-102">摘要</span><span class="sxs-lookup"><span data-stu-id="60ece-102">SYNOPSIS</span></span>
<span data-ttu-id="60ece-103">取得一或多個伺服器管理閘道。</span><span class="sxs-lookup"><span data-stu-id="60ece-103">Gets one or more Server Management Gateways.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60ece-104">句法</span><span class="sxs-lookup"><span data-stu-id="60ece-104">SYNTAX</span></span>

### <span data-ttu-id="60ece-105">NoParams (預設) </span><span class="sxs-lookup"><span data-stu-id="60ece-105">NoParams (Default)</span></span>
```
Get-AzureRmServerManagementGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60ece-106">Many-ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="60ece-106">Many-ByResourceGroup</span></span>
```
Get-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="60ece-107">Single-ByName</span><span class="sxs-lookup"><span data-stu-id="60ece-107">Single-ByName</span></span>
```
Get-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60ece-108">Single-ByObject</span><span class="sxs-lookup"><span data-stu-id="60ece-108">Single-ByObject</span></span>
```
Get-AzureRmServerManagementGateway [-Gateway] <Gateway> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="60ece-109">說明</span><span class="sxs-lookup"><span data-stu-id="60ece-109">DESCRIPTION</span></span>
<span data-ttu-id="60ece-110">**AzureRmServerManagementGateway** Cmdlet 會取得一或多個 Azure 伺服器管理閘道。</span><span class="sxs-lookup"><span data-stu-id="60ece-110">The **Get-AzureRmServerManagementGateway** cmdlet gets one or more Azure Server Management Gateways.</span></span>

## <span data-ttu-id="60ece-111">示例</span><span class="sxs-lookup"><span data-stu-id="60ece-111">EXAMPLES</span></span>

### <span data-ttu-id="60ece-112">範例1：取得訂閱中的所有閘道</span><span class="sxs-lookup"><span data-stu-id="60ece-112">Example 1: Get all gateways in a subscription</span></span>
```
PS C:\>Get-AzureRmServerManagementGateway
Resource Group Location       Auto Upgrade Gateway Name
-------------- --------       ------------ ------------
groupOne       centralus      Off          mygateway
groupOne       centralus      Off          othergateway
groupTwo       centralus      On           privategateway
```

<span data-ttu-id="60ece-113">這個命令會取得訂閱中的所有伺服器管理閘道。</span><span class="sxs-lookup"><span data-stu-id="60ece-113">This command gets all Server Management Gateways in the subscription.</span></span>

### <span data-ttu-id="60ece-114">範例2：在資源群組中取得閘道</span><span class="sxs-lookup"><span data-stu-id="60ece-114">Example 2: Get gateways in a resource group</span></span>
```
PS C:\>Get-AzureRmServerManagementGateway -ResourceGroupName "Group001"
Resource Group Location       Auto Upgrade Gateway Name
-------------- --------       ------------ ------------
myGroup        centralus      Off          mygateway
```

<span data-ttu-id="60ece-115">這個命令會取得屬於名為 Group001 之資源群組的所有伺服器管理閘道。</span><span class="sxs-lookup"><span data-stu-id="60ece-115">This command gets all Server Management Gateways that belong to the resource group named Group001.</span></span>

### <span data-ttu-id="60ece-116">範例3：取得所有已安裝的閘道實例</span><span class="sxs-lookup"><span data-stu-id="60ece-116">Example 3: Get all installed instances of a gateway</span></span>
```
PS C:\>(Get-AzureRmServerManagementGateway -ResourceGroupName "Group002" -GatewayName "Gateway01").Instances
Name             Installed              Version         Operating System
----             ---------              -------         ----------------
GATEWAYPC        4/13/2016 6:35:04 PM   1.0.1104.0      Microsoft Windows 10 Enterprise
```

<span data-ttu-id="60ece-117">這個命令會從屬於名為 Group002 之資源群組的所有名為 Gateway01 的伺服器管理閘道的所有實例中取得。</span><span class="sxs-lookup"><span data-stu-id="60ece-117">This command gets all instances of a Server Management Gateway named Gateway01 that belong to the resource group named Group002.</span></span>

## <span data-ttu-id="60ece-118">參數</span><span class="sxs-lookup"><span data-stu-id="60ece-118">PARAMETERS</span></span>

### <span data-ttu-id="60ece-119">-閘道</span><span class="sxs-lookup"><span data-stu-id="60ece-119">-Gateway</span></span>
<span data-ttu-id="60ece-120">指定此 Cmdlet 取得的閘道。</span><span class="sxs-lookup"><span data-stu-id="60ece-120">Specifies a gateway that this cmdlet gets.</span></span>

<span data-ttu-id="60ece-121">此 Cmdlet 會透過指定的閘道使用 *ResourceGroupName* 和 *GatewayName* 參數來執行動作。</span><span class="sxs-lookup"><span data-stu-id="60ece-121">The cmdlet uses the *ResourceGroupName* and *GatewayName* parameters through the specified Gateway to perform the action.</span></span>

<span data-ttu-id="60ece-122">指定此參數時，此 Cmdlet 將會包含閘道的詳細狀態。</span><span class="sxs-lookup"><span data-stu-id="60ece-122">When this parameter is specified, this cmdlet will include detailed status for the gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Gateway
Parameter Sets: Single-ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60ece-123">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="60ece-123">-GatewayName</span></span>
<span data-ttu-id="60ece-124">指定此 Cmdlet 取得入口的伺服器管理閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="60ece-124">Specifies the name of the Server Management Gateway for which this cmdlet gets gate.</span></span>

<span data-ttu-id="60ece-125">當您指定 *GatewayName* 參數時，此 Cmdlet 會在閘道上包含詳細的狀態。</span><span class="sxs-lookup"><span data-stu-id="60ece-125">When you specify the *GatewayName* parameter, this cmdlet will include detailed status on the gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: Single-ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60ece-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60ece-126">-ResourceGroupName</span></span>
<span data-ttu-id="60ece-127">指定此 Cmdlet 取得閘道的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="60ece-127">Specifies the name of the resource group for which this cmdlet gets gateways.</span></span>

```yaml
Type: System.String
Parameter Sets: Many-ByResourceGroup, Single-ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60ece-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60ece-128">-DefaultProfile</span></span>
<span data-ttu-id="60ece-129">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="60ece-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60ece-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60ece-130">CommonParameters</span></span>
<span data-ttu-id="60ece-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="60ece-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60ece-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="60ece-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60ece-133">輸入</span><span class="sxs-lookup"><span data-stu-id="60ece-133">INPUTS</span></span>

### <span data-ttu-id="60ece-134">關</span><span class="sxs-lookup"><span data-stu-id="60ece-134">Gateway</span></span>
<span data-ttu-id="60ece-135">參數 "閘道" 接受管線中 "Gateway" 類型的值</span><span class="sxs-lookup"><span data-stu-id="60ece-135">Parameter 'Gateway' accepts value of type 'Gateway' from the pipeline</span></span>

## <span data-ttu-id="60ece-136">輸出</span><span class="sxs-lookup"><span data-stu-id="60ece-136">OUTPUTS</span></span>

### <span data-ttu-id="60ece-137">[ServerManagement] 閘道</span><span class="sxs-lookup"><span data-stu-id="60ece-137">Microsoft.Azure.Commands.ServerManagement.Model.Gateway</span></span>

## <span data-ttu-id="60ece-138">筆記</span><span class="sxs-lookup"><span data-stu-id="60ece-138">NOTES</span></span>
* <span data-ttu-id="60ece-139">如果這個 Cmdlet 不使用參數，則會傳回與訂閱相關聯的所有閘道。</span><span class="sxs-lookup"><span data-stu-id="60ece-139">If this cmdlet is use without parameters, it will return all the gateways associated with the subscription.</span></span>

## <span data-ttu-id="60ece-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="60ece-140">RELATED LINKS</span></span>

[<span data-ttu-id="60ece-141">新-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="60ece-141">New-AzureRmServerManagementGateway</span></span>](./New-AzureRmServerManagementGateway.md)

[<span data-ttu-id="60ece-142">移除-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="60ece-142">Remove-AzureRmServerManagementGateway</span></span>](./Remove-AzureRmServerManagementGateway.md)


