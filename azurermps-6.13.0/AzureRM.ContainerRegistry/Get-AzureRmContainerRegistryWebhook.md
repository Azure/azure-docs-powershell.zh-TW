---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/get-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryWebhook.md
ms.openlocfilehash: d2fee7d402ddf25a2bcc4b32528e31e44f500618
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454667"
---
# <span data-ttu-id="e27bf-101">Get-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="e27bf-101">Get-AzureRmContainerRegistryWebhook</span></span>

## <span data-ttu-id="e27bf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e27bf-102">SYNOPSIS</span></span>
<span data-ttu-id="e27bf-103">取得容器註冊 webhook。</span><span class="sxs-lookup"><span data-stu-id="e27bf-103">Gets a container registry webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e27bf-104">句法</span><span class="sxs-lookup"><span data-stu-id="e27bf-104">SYNTAX</span></span>

### <span data-ttu-id="e27bf-105">ListWebhookByNameResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e27bf-105">ListWebhookByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistryWebhook [-ResourceGroupName] <String> [-RegistryName] <String>
 [-IncludeConfiguration] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e27bf-106">ShowWebhookByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="e27bf-106">ShowWebhookByNameResourceGroupParameterSet</span></span>
```
Get-AzureRmContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-IncludeConfiguration] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e27bf-107">ShowWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e27bf-107">ShowWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryWebhook [-Name] <String> -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e27bf-108">ListWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e27bf-108">ListWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryWebhook -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e27bf-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e27bf-109">ResourceIdParameterSet</span></span>
```
Get-AzureRmContainerRegistryWebhook [-IncludeConfiguration] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e27bf-110">說明</span><span class="sxs-lookup"><span data-stu-id="e27bf-110">DESCRIPTION</span></span>
<span data-ttu-id="e27bf-111">Get-AzureRmContainerRegistryWebhook Cmdlet 會取得容器登錄的指定 webhook，或容器註冊的所有 webhooks。</span><span class="sxs-lookup"><span data-stu-id="e27bf-111">The Get-AzureRmContainerRegistryWebhook cmdlet gets a specified webhook of container registry or all the webhooks of a container registry.</span></span>

## <span data-ttu-id="e27bf-112">示例</span><span class="sxs-lookup"><span data-stu-id="e27bf-112">EXAMPLES</span></span>

### <span data-ttu-id="e27bf-113">範例1：取得容器註冊的指定 webhook</span><span class="sxs-lookup"><span data-stu-id="e27bf-113">Example 1: Get a specified webhook of a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded
```

<span data-ttu-id="e27bf-114">取得容器註冊的指定 webhook</span><span class="sxs-lookup"><span data-stu-id="e27bf-114">Get a specified webhook of a container registry</span></span>

### <span data-ttu-id="e27bf-115">範例2：取得容器註冊的所有 webhooks</span><span class="sxs-lookup"><span data-stu-id="e27bf-115">Example 2: Get all the webhooks of a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook04       westus     enabled                    {push, delete}  Succeeded
webhook05       westus     disabled                   {push, delete}  Succeeded
wh003           westus     enabled                    delete          Succeeded
```

<span data-ttu-id="e27bf-116">取得容器註冊的所有 webhooks</span><span class="sxs-lookup"><span data-stu-id="e27bf-116">Get all the webhooks of a container registry</span></span>

### <span data-ttu-id="e27bf-117">範例3：使用配置詳細資料取得容器登錄的指定 webhook</span><span class="sxs-lookup"><span data-stu-id="e27bf-117">Example 3: Get a specified webhook of a container registry with configuration details</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -IncludeConfiguration

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded  http://www.test.com/
```

<span data-ttu-id="e27bf-118">使用配置詳細資料取得容器註冊表的指定 webhook</span><span class="sxs-lookup"><span data-stu-id="e27bf-118">Get a specified webhook of a container registry with configuration details</span></span>

## <span data-ttu-id="e27bf-119">參數</span><span class="sxs-lookup"><span data-stu-id="e27bf-119">PARAMETERS</span></span>

### <span data-ttu-id="e27bf-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e27bf-120">-DefaultProfile</span></span>
<span data-ttu-id="e27bf-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e27bf-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e27bf-122">-IncludeConfiguration</span><span class="sxs-lookup"><span data-stu-id="e27bf-122">-IncludeConfiguration</span></span>
<span data-ttu-id="e27bf-123">取得 webhook 的設定資訊。</span><span class="sxs-lookup"><span data-stu-id="e27bf-123">Get the configuration information for a webhook.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e27bf-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="e27bf-124">-Name</span></span>
<span data-ttu-id="e27bf-125">Webhook 名稱。</span><span class="sxs-lookup"><span data-stu-id="e27bf-125">Webhook Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ShowWebhookByNameResourceGroupParameterSet, ShowWebhookByRegistryObjectParameterSet
Aliases: WebhookName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e27bf-126">-Registry</span><span class="sxs-lookup"><span data-stu-id="e27bf-126">-Registry</span></span>
<span data-ttu-id="e27bf-127">分枝 Registry 物件。</span><span class="sxs-lookup"><span data-stu-id="e27bf-127">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: ShowWebhookByRegistryObjectParameterSet, ListWebhookByRegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e27bf-128">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="e27bf-128">-RegistryName</span></span>
<span data-ttu-id="e27bf-129">容器登錄名。</span><span class="sxs-lookup"><span data-stu-id="e27bf-129">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListWebhookByNameResourceGroupParameterSet, ShowWebhookByNameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e27bf-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e27bf-130">-ResourceGroupName</span></span>
<span data-ttu-id="e27bf-131">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="e27bf-131">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListWebhookByNameResourceGroupParameterSet, ShowWebhookByNameResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e27bf-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e27bf-132">-ResourceId</span></span>
<span data-ttu-id="e27bf-133">容器登錄 Webhook 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="e27bf-133">The container registry Webhook resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e27bf-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e27bf-134">CommonParameters</span></span>
<span data-ttu-id="e27bf-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e27bf-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e27bf-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e27bf-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e27bf-137">輸入</span><span class="sxs-lookup"><span data-stu-id="e27bf-137">INPUTS</span></span>

### <span data-ttu-id="e27bf-138">PSContainerRegistry 中的 ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e27bf-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>
<span data-ttu-id="e27bf-139">參數： Registry (ByValue) </span><span class="sxs-lookup"><span data-stu-id="e27bf-139">Parameters: Registry (ByValue)</span></span>

### <span data-ttu-id="e27bf-140">System.object</span><span class="sxs-lookup"><span data-stu-id="e27bf-140">System.String</span></span>

## <span data-ttu-id="e27bf-141">輸出</span><span class="sxs-lookup"><span data-stu-id="e27bf-141">OUTPUTS</span></span>

### <span data-ttu-id="e27bf-142">PSContainerRegistryWebhook 中的 ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e27bf-142">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="e27bf-143">筆記</span><span class="sxs-lookup"><span data-stu-id="e27bf-143">NOTES</span></span>

## <span data-ttu-id="e27bf-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="e27bf-144">RELATED LINKS</span></span>

[<span data-ttu-id="e27bf-145">新-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="e27bf-145">New-AzureRmContainerRegistryWebhook</span></span>](New-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="e27bf-146">更新-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="e27bf-146">Update-AzureRmContainerRegistryWebhook</span></span>](Update-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="e27bf-147">移除-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="e27bf-147">Remove-AzureRmContainerRegistryWebhook</span></span>](Remove-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="e27bf-148">Test-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="e27bf-148">Test-AzureRmContainerRegistryWebhook</span></span>](Test-AzureRmContainerRegistryWebhook.md)
