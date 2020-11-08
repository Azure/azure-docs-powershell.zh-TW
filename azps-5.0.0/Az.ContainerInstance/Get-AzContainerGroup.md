---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerinstance/get-azcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Get-AzContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Get-AzContainerGroup.md
ms.openlocfilehash: 2dadcac9f0b537a52a0a7270b7d20fc08e80461c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138194"
---
# <span data-ttu-id="d95b1-101">Get-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="d95b1-101">Get-AzContainerGroup</span></span>

## <span data-ttu-id="d95b1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d95b1-102">SYNOPSIS</span></span>
<span data-ttu-id="d95b1-103">取得容器群組。</span><span class="sxs-lookup"><span data-stu-id="d95b1-103">Gets container groups.</span></span>

## <span data-ttu-id="d95b1-104">句法</span><span class="sxs-lookup"><span data-stu-id="d95b1-104">SYNTAX</span></span>

### <span data-ttu-id="d95b1-105">ListContainerGroupParamSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d95b1-105">ListContainerGroupParamSet (Default)</span></span>
```
Get-AzContainerGroup [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d95b1-106">GetContainerGroupInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="d95b1-106">GetContainerGroupInResourceGroupParamSet</span></span>
```
Get-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d95b1-107">GetContainerGroupByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="d95b1-107">GetContainerGroupByResourceIdParamSet</span></span>
```
Get-AzContainerGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d95b1-108">說明</span><span class="sxs-lookup"><span data-stu-id="d95b1-108">DESCRIPTION</span></span>
<span data-ttu-id="d95b1-109">**AzContainerGroup** Cmdlet 會取得指定的容器群組或資源群組中的所有容器群組或訂閱。</span><span class="sxs-lookup"><span data-stu-id="d95b1-109">The **Get-AzContainerGroup** cmdlet gets a specified container group or all the container groups in a resource group or the subscription.</span></span>

## <span data-ttu-id="d95b1-110">示例</span><span class="sxs-lookup"><span data-stu-id="d95b1-110">EXAMPLES</span></span>

### <span data-ttu-id="d95b1-111">範例1：取得指定的容器群組</span><span class="sxs-lookup"><span data-stu-id="d95b1-111">Example 1: Gets a specified container group</span></span>
```
PS C:\> Get-AzContainerGroup -ResourceGroupName demo -Name mycontainer

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Succeeded
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {8000}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="d95b1-112">命令會取得指定的容器群組。</span><span class="sxs-lookup"><span data-stu-id="d95b1-112">The command gets the specified container group.</span></span>

### <span data-ttu-id="d95b1-113">範例2：取得資源群組中的容器群組</span><span class="sxs-lookup"><span data-stu-id="d95b1-113">Example 2: Gets container groups in a resource group</span></span>
```
PS C:\> Get-AzContainerGroup -ResourceGroupName demo

ResourceGroupName Name                     Location   OsType  Image                         IP                   Resources        ProvisioningState
----------------- ----                     --------   ------  -----                         --                   ---------        -----------------
demo              container1               west us    Linux   alpine:latest                 40.83.144.50:8002    1 cores/1 gb             Succeeded
demo              container2               west us    Linux   alpine:latest                 104.42.228.253:8001  1 cores/1 gb             Succeeded
```

<span data-ttu-id="d95b1-114">此命令會取得 [資源] 群組中的容器群組 `demo` 。</span><span class="sxs-lookup"><span data-stu-id="d95b1-114">The command gets the container groups in the resource group `demo`.</span></span>

### <span data-ttu-id="d95b1-115">範例3：在目前的訂閱中取得容器群組</span><span class="sxs-lookup"><span data-stu-id="d95b1-115">Example 3: Gets container groups in the current subscription</span></span>
```
PS C:\> Get-AzContainerGroup

ResourceGroupName Name                     Location   OsType  Image                         IP                   Resources        ProvisioningState
----------------- ----                     --------   ------  -----                         --                   ---------        -----------------
demo1             container1               west us    Linux   alpine:latest                 40.83.144.50:8002    1 cores/1 gb             Succeeded
demo2             container2               west us    Linux   alpine:latest                 104.42.228.253:8001  1 cores/1 gb             Succeeded
```

<span data-ttu-id="d95b1-116">命令會在目前的訂閱中取得容器群組。</span><span class="sxs-lookup"><span data-stu-id="d95b1-116">The command gets the container groups in the current subscription.</span></span>

### <span data-ttu-id="d95b1-117">範例4：使用資源識別碼取得容器群組。</span><span class="sxs-lookup"><span data-stu-id="d95b1-117">Example 4: Gets container groups using resource Id.</span></span>
```
PS C:\> Find-AzResource -ResourceGroupEquals demo -ResourceNameEquals mycontainer | Get-AzContainerGroup

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Succeeded
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {8000}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="d95b1-118">命令會取得擁有資源識別碼的容器群組。</span><span class="sxs-lookup"><span data-stu-id="d95b1-118">The command gets the container group with the resource Id.</span></span>

## <span data-ttu-id="d95b1-119">參數</span><span class="sxs-lookup"><span data-stu-id="d95b1-119">PARAMETERS</span></span>

### <span data-ttu-id="d95b1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d95b1-120">-DefaultProfile</span></span>
<span data-ttu-id="d95b1-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d95b1-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d95b1-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="d95b1-122">-Name</span></span>
<span data-ttu-id="d95b1-123">容器組名。</span><span class="sxs-lookup"><span data-stu-id="d95b1-123">The container group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetContainerGroupInResourceGroupParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d95b1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d95b1-124">-ResourceGroupName</span></span>
<span data-ttu-id="d95b1-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d95b1-125">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListContainerGroupParamSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetContainerGroupInResourceGroupParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d95b1-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d95b1-126">-ResourceId</span></span>
<span data-ttu-id="d95b1-127">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="d95b1-127">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetContainerGroupByResourceIdParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d95b1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d95b1-128">CommonParameters</span></span>
<span data-ttu-id="d95b1-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d95b1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d95b1-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d95b1-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d95b1-131">輸入</span><span class="sxs-lookup"><span data-stu-id="d95b1-131">INPUTS</span></span>

### <span data-ttu-id="d95b1-132">System.object</span><span class="sxs-lookup"><span data-stu-id="d95b1-132">System.String</span></span>

## <span data-ttu-id="d95b1-133">輸出</span><span class="sxs-lookup"><span data-stu-id="d95b1-133">OUTPUTS</span></span>

### <span data-ttu-id="d95b1-134">PSContainerGroup 中的 ContainerInstance。</span><span class="sxs-lookup"><span data-stu-id="d95b1-134">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="d95b1-135">筆記</span><span class="sxs-lookup"><span data-stu-id="d95b1-135">NOTES</span></span>

## <span data-ttu-id="d95b1-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="d95b1-136">RELATED LINKS</span></span>
