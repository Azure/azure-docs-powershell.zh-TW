---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: AFF75E0B-CB88-45ED-9067-7F43E2BA485C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzContainerService.md
ms.openlocfilehash: 9d8afa31d296e62c75b869bd93e6f96aadf82328
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613422"
---
# <span data-ttu-id="270ca-101">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="270ca-101">Get-AzContainerService</span></span>

## <span data-ttu-id="270ca-102">摘要</span><span class="sxs-lookup"><span data-stu-id="270ca-102">SYNOPSIS</span></span>
<span data-ttu-id="270ca-103">取得容器服務。</span><span class="sxs-lookup"><span data-stu-id="270ca-103">Gets a container service.</span></span>

## <span data-ttu-id="270ca-104">句法</span><span class="sxs-lookup"><span data-stu-id="270ca-104">SYNTAX</span></span>

```
Get-AzContainerService [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="270ca-105">說明</span><span class="sxs-lookup"><span data-stu-id="270ca-105">DESCRIPTION</span></span>
<span data-ttu-id="270ca-106">**AzContainerService** Cmdlet 會取得容器服務。</span><span class="sxs-lookup"><span data-stu-id="270ca-106">The **Get-AzContainerService** cmdlet gets a container service.</span></span>
<span data-ttu-id="270ca-107">您可以查看容器服務的屬性，其中包括狀態、主版和代理程式的數目，以及主要和代理程式的完整功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="270ca-107">You can view the properties of a container service, which include state, number of master and agents, and fully qualified domain name of master and agent.</span></span>

## <span data-ttu-id="270ca-108">示例</span><span class="sxs-lookup"><span data-stu-id="270ca-108">EXAMPLES</span></span>

### <span data-ttu-id="270ca-109">範例1：取得容器服務</span><span class="sxs-lookup"><span data-stu-id="270ca-109">Example 1: Get a container service</span></span>
```
PS C:\> Get-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"

ResourceGroupName     : ResourceGroup17
ProvisioningState     : Succeeded
OrchestratorProfile   :
  OrchestratorType    : DCOS
MasterProfile         :
  Count               : 1
  DnsPrefix           : MasterResourceGroup17
  Fqdn                : masterresourcegroup17.eastus.cloudapp.azure.com
AgentPoolProfiles[0]  :
  Name                : AgentPool01
  Count               : 2
  VmSize              : Standard_A1
  DnsPrefix           : APResourceGroup17
  Fqdn                : apresourcegroup17.eastus.cloudapp.azure.com
LinuxProfile          :
  AdminUsername       : acslinuxadmin
  Ssh                 :
    PublicKeys[0]     :
      KeyData         : ssh-rsa xxxxxxxxxxxxxx contoso@microsoft.com
DiagnosticsProfile    :
  VmDiagnostics       :
    Enabled           : False
    StorageUri        : https://xxxxxxxxxxx.blob.core.windows.net/
Id                    : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup17/providers/Micr
osoft.ContainerService/containerServices/CSResourceGroup17
Name                  : CSResourceGroup17
Type                  : Microsoft.ContainerService/ContainerServices
Location              : eastus
Tags                  : {}
```

<span data-ttu-id="270ca-110">這個命令會取得名為 CSResourceGroup17 的容器服務。</span><span class="sxs-lookup"><span data-stu-id="270ca-110">This command gets a container service named CSResourceGroup17.</span></span>

### <span data-ttu-id="270ca-111">範例2：取得所有容器服務</span><span class="sxs-lookup"><span data-stu-id="270ca-111">Example 2: Get all container services</span></span>
```
PS C:\> Get-AzContainerService

ResourceGroupName   Name                Location ProvisioningState
-----------------   ----                -------- -----------------
ResourceGroup17     CSResourceGroup17   eastus         Succeeded
ResourceGroup17     CSResourceGroup18   eastus         Succeeded
ResourceGroup18     CSResourceGroup19   eastus         Succeeded
ResourceGroup18     CSResourceGroup20   eastus         Succeeded
```

<span data-ttu-id="270ca-112">這個命令會取得訂閱中的所有容器服務。</span><span class="sxs-lookup"><span data-stu-id="270ca-112">This command gets all container services in subscription.</span></span>

### <span data-ttu-id="270ca-113">範例3：取得資源群組中的所有容器服務</span><span class="sxs-lookup"><span data-stu-id="270ca-113">Example 3: Get all container services in resource group</span></span>
```
PS C:\> Get-AzContainerService -ResourceGroupName "ResourceGroup17"

ResourceGroupName   Name                Location ProvisioningState
-----------------   ----                -------- -----------------
ResourceGroup17     CSResourceGroup17   eastus         Succeeded
ResourceGroup17     CSResourceGroup18   eastus         Succeeded
```

<span data-ttu-id="270ca-114">這個命令會在 ResourceGroup17 中取得所有容器服務。</span><span class="sxs-lookup"><span data-stu-id="270ca-114">This command gets all container services in ResourceGroup17.</span></span>

### <span data-ttu-id="270ca-115">範例4：使用篩選取得所有容器服務</span><span class="sxs-lookup"><span data-stu-id="270ca-115">Example 4: Get all container services using filter</span></span>
```
PS C:\> Get-AzContainerService -Name "CSResourceGroup1*"

ResourceGroupName   Name                Location ProvisioningState
-----------------   ----                -------- -----------------
ResourceGroup17     CSResourceGroup17   eastus         Succeeded
ResourceGroup17     CSResourceGroup18   eastus         Succeeded
ResourceGroup18     CSResourceGroup19   eastus         Succeeded
```

<span data-ttu-id="270ca-116">這個命令會取得所有以 "CSResourceGroup1" 為開頭的容器服務。</span><span class="sxs-lookup"><span data-stu-id="270ca-116">This command gets all container services starting with "CSResourceGroup1".</span></span>

## <span data-ttu-id="270ca-117">參數</span><span class="sxs-lookup"><span data-stu-id="270ca-117">PARAMETERS</span></span>

### <span data-ttu-id="270ca-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="270ca-118">-DefaultProfile</span></span>
<span data-ttu-id="270ca-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="270ca-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="270ca-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="270ca-120">-Name</span></span>
<span data-ttu-id="270ca-121">指定此 Cmdlet 所取得之容器服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="270ca-121">Specifies the name of the container service that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="270ca-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="270ca-122">-ResourceGroupName</span></span>
<span data-ttu-id="270ca-123">指定此 Cmdlet 所取得之容器服務的資源群組。</span><span class="sxs-lookup"><span data-stu-id="270ca-123">Specifies the resource group of the container service that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="270ca-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="270ca-124">CommonParameters</span></span>
<span data-ttu-id="270ca-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="270ca-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="270ca-126">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="270ca-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="270ca-127">輸入</span><span class="sxs-lookup"><span data-stu-id="270ca-127">INPUTS</span></span>

### <span data-ttu-id="270ca-128">System.object</span><span class="sxs-lookup"><span data-stu-id="270ca-128">System.String</span></span>

## <span data-ttu-id="270ca-129">輸出</span><span class="sxs-lookup"><span data-stu-id="270ca-129">OUTPUTS</span></span>

### <span data-ttu-id="270ca-130">PSContainerService 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="270ca-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="270ca-131">筆記</span><span class="sxs-lookup"><span data-stu-id="270ca-131">NOTES</span></span>

## <span data-ttu-id="270ca-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="270ca-132">RELATED LINKS</span></span>

[<span data-ttu-id="270ca-133">新-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="270ca-133">New-AzContainerService</span></span>](./New-AzContainerService.md)

[<span data-ttu-id="270ca-134">移除-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="270ca-134">Remove-AzContainerService</span></span>](./Remove-AzContainerService.md)

[<span data-ttu-id="270ca-135">更新-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="270ca-135">Update-AzContainerService</span></span>](./Update-AzContainerService.md)


