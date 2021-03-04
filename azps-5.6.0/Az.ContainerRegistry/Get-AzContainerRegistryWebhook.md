---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/get-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryWebhook.md
ms.openlocfilehash: 36bc713561c739804b358e4b778e17740bd9fb6a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908290"
---
# <span data-ttu-id="c2962-101">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="c2962-101">Get-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="c2962-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c2962-102">SYNOPSIS</span></span>
<span data-ttu-id="c2962-103">獲得容器註冊表網頁。</span><span class="sxs-lookup"><span data-stu-id="c2962-103">Gets a container registry webhook.</span></span>

## <span data-ttu-id="c2962-104">語法</span><span class="sxs-lookup"><span data-stu-id="c2962-104">SYNTAX</span></span>

### <span data-ttu-id="c2962-105">ListWebgroupByNameResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c2962-105">ListWebhookByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryWebhook [-ResourceGroupName] <String> [-RegistryName] <String> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2962-106">ShowWeb有ByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2962-106">ShowWebhookByNameResourceGroupParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-IncludeConfiguration] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2962-107">ShowWeb有ByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2962-107">ShowWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-Name] <String> -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2962-108">ListWeb有ByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2962-108">ListWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryWebhook -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2962-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2962-109">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-IncludeConfiguration] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2962-110">描述</span><span class="sxs-lookup"><span data-stu-id="c2962-110">DESCRIPTION</span></span>
<span data-ttu-id="c2962-111">此Get-AzContainerRegistryWebhook Cmdlet 會獲得指定的容器註冊表網頁元件，或容器註冊表的所有網頁元件。</span><span class="sxs-lookup"><span data-stu-id="c2962-111">The Get-AzContainerRegistryWebhook cmdlet gets a specified webhook of container registry or all the webhooks of a container registry.</span></span>

## <span data-ttu-id="c2962-112">例子</span><span class="sxs-lookup"><span data-stu-id="c2962-112">EXAMPLES</span></span>

### <span data-ttu-id="c2962-113">範例 1：取得容器註冊表的指定網頁元件</span><span class="sxs-lookup"><span data-stu-id="c2962-113">Example 1: Get a specified webhook of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded
```

<span data-ttu-id="c2962-114">取得容器註冊表的指定網頁元件</span><span class="sxs-lookup"><span data-stu-id="c2962-114">Get a specified webhook of a container registry</span></span>

### <span data-ttu-id="c2962-115">範例 2：取得容器註冊表的所有網頁元件</span><span class="sxs-lookup"><span data-stu-id="c2962-115">Example 2: Get all the webhooks of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook04       westus     enabled                    {push, delete}  Succeeded
webhook05       westus     disabled                   {push, delete}  Succeeded
wh003           westus     enabled                    delete          Succeeded
```

<span data-ttu-id="c2962-116">取得容器註冊表的所有網頁元件</span><span class="sxs-lookup"><span data-stu-id="c2962-116">Get all the webhooks of a container registry</span></span>

### <span data-ttu-id="c2962-117">範例 3：取得具有組組詳細資料之容器註冊表的指定 Web功能</span><span class="sxs-lookup"><span data-stu-id="c2962-117">Example 3: Get a specified webhook of a container registry with configuration details</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -IncludeConfiguration

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded  http://www.test.com/
```

<span data-ttu-id="c2962-118">取得具有組組詳細資料之容器註冊表的指定網頁元件</span><span class="sxs-lookup"><span data-stu-id="c2962-118">Get a specified webhook of a container registry with configuration details</span></span>

## <span data-ttu-id="c2962-119">參數</span><span class="sxs-lookup"><span data-stu-id="c2962-119">PARAMETERS</span></span>

### <span data-ttu-id="c2962-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2962-120">-DefaultProfile</span></span>
<span data-ttu-id="c2962-121">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c2962-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2962-122">-IncludeConfiguration</span><span class="sxs-lookup"><span data-stu-id="c2962-122">-IncludeConfiguration</span></span>
<span data-ttu-id="c2962-123">取得網頁的組組資訊。</span><span class="sxs-lookup"><span data-stu-id="c2962-123">Get the configuration information for a webhook.</span></span>

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

### <span data-ttu-id="c2962-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="c2962-124">-Name</span></span>
<span data-ttu-id="c2962-125">Web下一個名稱。</span><span class="sxs-lookup"><span data-stu-id="c2962-125">Webhook Name.</span></span>

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

### <span data-ttu-id="c2962-126">-Registry</span><span class="sxs-lookup"><span data-stu-id="c2962-126">-Registry</span></span>
<span data-ttu-id="c2962-127">Container Registry 物件。</span><span class="sxs-lookup"><span data-stu-id="c2962-127">Container Registry Object.</span></span>

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

### <span data-ttu-id="c2962-128">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="c2962-128">-RegistryName</span></span>
<span data-ttu-id="c2962-129">容器註冊表名稱。</span><span class="sxs-lookup"><span data-stu-id="c2962-129">Container Registry Name.</span></span>

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

### <span data-ttu-id="c2962-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2962-130">-ResourceGroupName</span></span>
<span data-ttu-id="c2962-131">資源組名。</span><span class="sxs-lookup"><span data-stu-id="c2962-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="c2962-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2962-132">-ResourceId</span></span>
<span data-ttu-id="c2962-133">容器登錄 Web方資源識別碼</span><span class="sxs-lookup"><span data-stu-id="c2962-133">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="c2962-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2962-134">CommonParameters</span></span>
<span data-ttu-id="c2962-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c2962-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2962-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c2962-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2962-137">輸入</span><span class="sxs-lookup"><span data-stu-id="c2962-137">INPUTS</span></span>

### <span data-ttu-id="c2962-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c2962-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="c2962-139">System.String</span><span class="sxs-lookup"><span data-stu-id="c2962-139">System.String</span></span>

## <span data-ttu-id="c2962-140">輸出</span><span class="sxs-lookup"><span data-stu-id="c2962-140">OUTPUTS</span></span>

### <span data-ttu-id="c2962-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebtain</span><span class="sxs-lookup"><span data-stu-id="c2962-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="c2962-142">筆記</span><span class="sxs-lookup"><span data-stu-id="c2962-142">NOTES</span></span>

## <span data-ttu-id="c2962-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="c2962-143">RELATED LINKS</span></span>

[<span data-ttu-id="c2962-144">New-AzContainerRegistryWebtain</span><span class="sxs-lookup"><span data-stu-id="c2962-144">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="c2962-145">Update-AzContainerRegistryWebtain</span><span class="sxs-lookup"><span data-stu-id="c2962-145">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="c2962-146">Remove-AzContainerRegistryWebtain</span><span class="sxs-lookup"><span data-stu-id="c2962-146">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)

[<span data-ttu-id="c2962-147">Test-AzContainerRegistryWebtain</span><span class="sxs-lookup"><span data-stu-id="c2962-147">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)