---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/get-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryWebhook.md
ms.openlocfilehash: 4f20f177b172ab9b5372de6b95d821202e991000
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447844"
---
# <span data-ttu-id="3e9c1-101">Get-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="3e9c1-101">Get-AzureRmContainerRegistryWebhook</span></span>

## <span data-ttu-id="3e9c1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3e9c1-102">SYNOPSIS</span></span>
<span data-ttu-id="3e9c1-103">取得容器註冊 webhook。</span><span class="sxs-lookup"><span data-stu-id="3e9c1-103">Gets a container registry webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e9c1-104">句法</span><span class="sxs-lookup"><span data-stu-id="3e9c1-104">SYNTAX</span></span>

### <span data-ttu-id="3e9c1-105">ListWebhookByNameResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="3e9c1-105">ListWebhookByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistryWebhook [-ResourceGroupName] <String> [-RegistryName] <String>
 [-IncludeConfiguration] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e9c1-106">ShowWebhookByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e9c1-106">ShowWebhookByNameResourceGroupParameterSet</span></span>
```
Get-AzureRmContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-IncludeConfiguration] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e9c1-107">ShowWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e9c1-107">ShowWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryWebhook [-Name] <String> -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e9c1-108">ListWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e9c1-108">ListWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryWebhook -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e9c1-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e9c1-109">ResourceIdParameterSet</span></span>
```
Get-AzureRmContainerRegistryWebhook [-IncludeConfiguration] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e9c1-110">說明</span><span class="sxs-lookup"><span data-stu-id="3e9c1-110">DESCRIPTION</span></span>
<span data-ttu-id="3e9c1-111">Get-AzureRmContainerRegistryWebhook Cmdlet 會取得容器登錄的指定 webhook，或容器註冊的所有 webhooks。</span><span class="sxs-lookup"><span data-stu-id="3e9c1-111">The Get-AzureRmContainerRegistryWebhook cmdlet gets a specified webhook of container registry or all the webhooks of a container registry.</span></span>

## <span data-ttu-id="3e9c1-112">示例</span><span class="sxs-lookup"><span data-stu-id="3e9c1-112">EXAMPLES</span></span>

### <span data-ttu-id="3e9c1-113">範例1：取得容器註冊的指定 webhook</span><span class="sxs-lookup"><span data-stu-id="3e9c1-113">Example 1: Get a specified webhook of a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded
```

<span data-ttu-id="3e9c1-114">取得容器註冊的指定 webhook</span><span class="sxs-lookup"><span data-stu-id="3e9c1-114">Get a specified webhook of a container registry</span></span>

### <span data-ttu-id="3e9c1-115">範例2：取得容器註冊的所有 webhooks</span><span class="sxs-lookup"><span data-stu-id="3e9c1-115">Example 2: Get all the webhooks of a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook04       westus     enabled                    {push, delete}  Succeeded
webhook05       westus     disabled                   {push, delete}  Succeeded
wh003           westus     enabled                    delete          Succeeded
```

<span data-ttu-id="3e9c1-116">取得容器註冊的所有 webhooks</span><span class="sxs-lookup"><span data-stu-id="3e9c1-116">Get all the webhooks of a container registry</span></span>

### <span data-ttu-id="3e9c1-117">範例3：使用配置詳細資料取得容器登錄的指定 webhook</span><span class="sxs-lookup"><span data-stu-id="3e9c1-117">Example 3: Get a specified webhook of a container registry with configuration details</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -IncludeConfiguration

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded  http://www.test.com/
```

<span data-ttu-id="3e9c1-118">使用配置詳細資料取得容器註冊表的指定 webhook</span><span class="sxs-lookup"><span data-stu-id="3e9c1-118">Get a specified webhook of a container registry with configuration details</span></span>

## <span data-ttu-id="3e9c1-119">參數</span><span class="sxs-lookup"><span data-stu-id="3e9c1-119">PARAMETERS</span></span>

### <span data-ttu-id="3e9c1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e9c1-120">-DefaultProfile</span></span>
<span data-ttu-id="3e9c1-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3e9c1-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e9c1-122">-IncludeConfiguration</span><span class="sxs-lookup"><span data-stu-id="3e9c1-122">-IncludeConfiguration</span></span>
<span data-ttu-id="3e9c1-123">取得 webhook 的設定資訊。</span><span class="sxs-lookup"><span data-stu-id="3e9c1-123">Get the configuration information for a webhook.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e9c1-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="3e9c1-124">-Name</span></span>
<span data-ttu-id="3e9c1-125">Webhook 名稱。</span><span class="sxs-lookup"><span data-stu-id="3e9c1-125">Webhook Name.</span></span>

```yaml
Type: String
Parameter Sets: ShowWebhookByNameResourceGroupParameterSet, ShowWebhookByRegistryObjectParameterSet
Aliases: WebhookName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e9c1-126">-Registry</span><span class="sxs-lookup"><span data-stu-id="3e9c1-126">-Registry</span></span>
<span data-ttu-id="3e9c1-127">分枝 Registry 物件。</span><span class="sxs-lookup"><span data-stu-id="3e9c1-127">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistry
Parameter Sets: ShowWebhookByRegistryObjectParameterSet, ListWebhookByRegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3e9c1-128">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="3e9c1-128">-RegistryName</span></span>
<span data-ttu-id="3e9c1-129">容器登錄名。</span><span class="sxs-lookup"><span data-stu-id="3e9c1-129">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: ListWebhookByNameResourceGroupParameterSet, ShowWebhookByNameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e9c1-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e9c1-130">-ResourceGroupName</span></span>
<span data-ttu-id="3e9c1-131">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="3e9c1-131">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ListWebhookByNameResourceGroupParameterSet, ShowWebhookByNameResourceGroupParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e9c1-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3e9c1-132">-ResourceId</span></span>
<span data-ttu-id="3e9c1-133">容器登錄 Webhook 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="3e9c1-133">The container registry Webhook resource id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e9c1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e9c1-134">CommonParameters</span></span>
<span data-ttu-id="3e9c1-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3e9c1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e9c1-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3e9c1-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e9c1-137">輸入</span><span class="sxs-lookup"><span data-stu-id="3e9c1-137">INPUTS</span></span>

### <span data-ttu-id="3e9c1-138">PSContainerRegistry 中的 ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="3e9c1-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>
<span data-ttu-id="3e9c1-139">System.object</span><span class="sxs-lookup"><span data-stu-id="3e9c1-139">System.String</span></span>

## <span data-ttu-id="3e9c1-140">輸出</span><span class="sxs-lookup"><span data-stu-id="3e9c1-140">OUTPUTS</span></span>

### <span data-ttu-id="3e9c1-141">PSContainerRegistryWebhook 中的 ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="3e9c1-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>
<span data-ttu-id="3e9c1-142">ContainerRegistry 集合. 泛型. IList "1 [PSContainerRegistryWebhook，ContainerRegistry，版本 = 1.0.0.0，Culture = 中性，PublicKeyToken = null]] （"）]</span><span class="sxs-lookup"><span data-stu-id="3e9c1-142">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook, Microsoft.Azure.Commands.ContainerRegistry, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="3e9c1-143">筆記</span><span class="sxs-lookup"><span data-stu-id="3e9c1-143">NOTES</span></span>

## <span data-ttu-id="3e9c1-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="3e9c1-144">RELATED LINKS</span></span>

[<span data-ttu-id="3e9c1-145">新-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="3e9c1-145">New-AzureRmContainerRegistryWebhook</span></span>](New-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="3e9c1-146">更新-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="3e9c1-146">Update-AzureRmContainerRegistryWebhook</span></span>](Update-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="3e9c1-147">移除-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="3e9c1-147">Remove-AzureRmContainerRegistryWebhook</span></span>](Remove-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="3e9c1-148">Test-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="3e9c1-148">Test-AzureRmContainerRegistryWebhook</span></span>](Test-AzureRmContainerRegistryWebhook.md)
