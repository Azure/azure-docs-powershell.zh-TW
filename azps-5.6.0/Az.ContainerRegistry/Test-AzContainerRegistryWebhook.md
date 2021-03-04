---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/test-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryWebhook.md
ms.openlocfilehash: 837e0fa40bc07ce5c38d6dfd4b7c86efe2425be9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903005"
---
# <span data-ttu-id="bc830-101">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="bc830-101">Test-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="bc830-102">簡介</span><span class="sxs-lookup"><span data-stu-id="bc830-102">SYNOPSIS</span></span>
<span data-ttu-id="bc830-103">觸發 web一次 ping 事件。</span><span class="sxs-lookup"><span data-stu-id="bc830-103">Triggers a webhook ping event.</span></span>

## <span data-ttu-id="bc830-104">語法</span><span class="sxs-lookup"><span data-stu-id="bc830-104">SYNTAX</span></span>

### <span data-ttu-id="bc830-105">ResourceIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="bc830-105">ResourceIdParameterSet (Default)</span></span>
```
Test-AzContainerRegistryWebhook -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bc830-106">NameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc830-106">NameResourceGroupParameterSet</span></span>
```
Test-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc830-107">Web有ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc830-107">WebhookObjectParameterSet</span></span>
```
Test-AzContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc830-108">描述</span><span class="sxs-lookup"><span data-stu-id="bc830-108">DESCRIPTION</span></span>
<span data-ttu-id="bc830-109">此Test-AzContainerRegistryWebhook Cmdlet 會觸發 web一次 ping 事件。</span><span class="sxs-lookup"><span data-stu-id="bc830-109">The Test-AzContainerRegistryWebhook cmdlet triggers a webhook ping event.</span></span>

## <span data-ttu-id="bc830-110">例子</span><span class="sxs-lookup"><span data-stu-id="bc830-110">EXAMPLES</span></span>

### <span data-ttu-id="bc830-111">範例 1：觸發 web一次 ping 事件。</span><span class="sxs-lookup"><span data-stu-id="bc830-111">Example 1: Triggers a webhook ping event.</span></span>
```powershell
PS C:\> Test-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Id
--
c5950af0-c8d0-4924-9873-1ba7da5cbf83
```

<span data-ttu-id="bc830-112">觸發 web一次 ping 事件。</span><span class="sxs-lookup"><span data-stu-id="bc830-112">Triggers a webhook ping event.</span></span>

## <span data-ttu-id="bc830-113">參數</span><span class="sxs-lookup"><span data-stu-id="bc830-113">PARAMETERS</span></span>

### <span data-ttu-id="bc830-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc830-114">-DefaultProfile</span></span>
<span data-ttu-id="bc830-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="bc830-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc830-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="bc830-116">-Name</span></span>
<span data-ttu-id="bc830-117">Web下一個名稱。</span><span class="sxs-lookup"><span data-stu-id="bc830-117">Webhook Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: WebhookName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc830-118">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="bc830-118">-RegistryName</span></span>
<span data-ttu-id="bc830-119">容器註冊表名稱。</span><span class="sxs-lookup"><span data-stu-id="bc830-119">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc830-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc830-120">-ResourceGroupName</span></span>
<span data-ttu-id="bc830-121">資源組名。</span><span class="sxs-lookup"><span data-stu-id="bc830-121">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc830-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bc830-122">-ResourceId</span></span>
<span data-ttu-id="bc830-123">容器登錄 Web方資源識別碼</span><span class="sxs-lookup"><span data-stu-id="bc830-123">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="bc830-124">-Web上</span><span class="sxs-lookup"><span data-stu-id="bc830-124">-Webhook</span></span>
<span data-ttu-id="bc830-125">Container Registry 物件。</span><span class="sxs-lookup"><span data-stu-id="bc830-125">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook
Parameter Sets: WebhookObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc830-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc830-126">CommonParameters</span></span>
<span data-ttu-id="bc830-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="bc830-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc830-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bc830-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc830-129">輸入</span><span class="sxs-lookup"><span data-stu-id="bc830-129">INPUTS</span></span>

### <span data-ttu-id="bc830-130">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebtain</span><span class="sxs-lookup"><span data-stu-id="bc830-130">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="bc830-131">System.String</span><span class="sxs-lookup"><span data-stu-id="bc830-131">System.String</span></span>

## <span data-ttu-id="bc830-132">輸出</span><span class="sxs-lookup"><span data-stu-id="bc830-132">OUTPUTS</span></span>

### <span data-ttu-id="bc830-133">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryEventInfo</span><span class="sxs-lookup"><span data-stu-id="bc830-133">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryEventInfo</span></span>

## <span data-ttu-id="bc830-134">筆記</span><span class="sxs-lookup"><span data-stu-id="bc830-134">NOTES</span></span>

## <span data-ttu-id="bc830-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="bc830-135">RELATED LINKS</span></span>

[<span data-ttu-id="bc830-136">New-AzContainerRegistryWebtain</span><span class="sxs-lookup"><span data-stu-id="bc830-136">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="bc830-137">Get-AzContainerRegistryWebtain</span><span class="sxs-lookup"><span data-stu-id="bc830-137">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="bc830-138">Update-AzContainerRegistryWebtain</span><span class="sxs-lookup"><span data-stu-id="bc830-138">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="bc830-139">Remove-AzContainerRegistryWebtain</span><span class="sxs-lookup"><span data-stu-id="bc830-139">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)