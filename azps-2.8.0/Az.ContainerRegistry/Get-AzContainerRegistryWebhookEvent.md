---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistrywebhookevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryWebhookEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryWebhookEvent.md
ms.openlocfilehash: 9bd55d0454b26e7e8ac9106c4ff1004be7050235
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613072"
---
# <span data-ttu-id="0b780-101">Get-AzContainerRegistryWebhookEvent</span><span class="sxs-lookup"><span data-stu-id="0b780-101">Get-AzContainerRegistryWebhookEvent</span></span>

## <span data-ttu-id="0b780-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0b780-102">SYNOPSIS</span></span>
<span data-ttu-id="0b780-103">取得容器註冊 webhook 的事件。</span><span class="sxs-lookup"><span data-stu-id="0b780-103">Gets events of a container registry webhook.</span></span>

## <span data-ttu-id="0b780-104">句法</span><span class="sxs-lookup"><span data-stu-id="0b780-104">SYNTAX</span></span>

### <span data-ttu-id="0b780-105">ListWebhookEventsByNameResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="0b780-105">ListWebhookEventsByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryWebhookEvent [-WebhookName] <String> [-ResourceGroupName] <String>
 [-RegistryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0b780-106">ListWebhookEventsByWebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b780-106">ListWebhookEventsByWebhookObjectParameterSet</span></span>
```
Get-AzContainerRegistryWebhookEvent -Webhook <PSContainerRegistryWebhook>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0b780-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b780-107">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryWebhookEvent -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0b780-108">說明</span><span class="sxs-lookup"><span data-stu-id="0b780-108">DESCRIPTION</span></span>
<span data-ttu-id="0b780-109">Get-AzContainerRegistryWebhookEvent Cmdlet 會列出 webhook 的所有事件。</span><span class="sxs-lookup"><span data-stu-id="0b780-109">The Get-AzContainerRegistryWebhookEvent cmdlet lists all the events of a webhook.</span></span>

## <span data-ttu-id="0b780-110">示例</span><span class="sxs-lookup"><span data-stu-id="0b780-110">EXAMPLES</span></span>

### <span data-ttu-id="0b780-111">範例1：取得 webhook 的所有事件。</span><span class="sxs-lookup"><span data-stu-id="0b780-111">Example 1: Gets all the events of a webhook.</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhookEvent -ResourceGroupName mattacrtest001 -RegistryName premium001 -Name webhook001

   Webhook service Uri: http://www.bing.com/

ID                                       Action   Timestamp                      Response
                                                                                 StatusCode
--                                       ------   ---------                      ----------
3c6281b6-47cd-4129-948b-4036780236f0     ping     11/17/2017 5:10:09 PM          200
70f1d41d-15fe-4251-87b6-43c32a91eae7     ping     11/17/2017 6:56:23 AM          200
5d25556b-32d0-4377-8031-d8ba7a263d6a     ping     11/17/2017 6:27:41 AM          200
c1e7d8aa-9f1b-447c-9583-2a58b7f81026     ping     11/17/2017 12:09:41 AM         200
eb4aa503-0d14-4f25-8ae5-33cce9a8fd50     ping     11/16/2017 11:35:03 PM         200
85a93d7f-3923-4ec5-bb8e-9ded5b6549c1     ping     11/17/2017 5:10:09 PM          200
9e3c8b5f-e0ee-47cf-9727-df1c8d45a497     ping     11/17/2017 6:56:23 AM          200
2d0ce294-9b59-4f5c-953a-47f2b270526f     ping     11/17/2017 6:27:41 AM          200
```

<span data-ttu-id="0b780-112">取得 webhook 的所有事件。</span><span class="sxs-lookup"><span data-stu-id="0b780-112">Gets all the events of a webhook.</span></span>

## <span data-ttu-id="0b780-113">參數</span><span class="sxs-lookup"><span data-stu-id="0b780-113">PARAMETERS</span></span>

### <span data-ttu-id="0b780-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b780-114">-DefaultProfile</span></span>
<span data-ttu-id="0b780-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0b780-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b780-116">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="0b780-116">-RegistryName</span></span>
<span data-ttu-id="0b780-117">容器登錄名。</span><span class="sxs-lookup"><span data-stu-id="0b780-117">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListWebhookEventsByNameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b780-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b780-118">-ResourceGroupName</span></span>
<span data-ttu-id="0b780-119">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="0b780-119">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListWebhookEventsByNameResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b780-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0b780-120">-ResourceId</span></span>
<span data-ttu-id="0b780-121">容器登錄 Webhook 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="0b780-121">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="0b780-122">-Webhook</span><span class="sxs-lookup"><span data-stu-id="0b780-122">-Webhook</span></span>
<span data-ttu-id="0b780-123">分枝 Registry 物件。</span><span class="sxs-lookup"><span data-stu-id="0b780-123">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook
Parameter Sets: ListWebhookEventsByWebhookObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b780-124">-WebhookName</span><span class="sxs-lookup"><span data-stu-id="0b780-124">-WebhookName</span></span>
<span data-ttu-id="0b780-125">Webhook 名稱。</span><span class="sxs-lookup"><span data-stu-id="0b780-125">Webhook Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListWebhookEventsByNameResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b780-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b780-126">CommonParameters</span></span>
<span data-ttu-id="0b780-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0b780-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b780-128">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0b780-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b780-129">輸入</span><span class="sxs-lookup"><span data-stu-id="0b780-129">INPUTS</span></span>

### <span data-ttu-id="0b780-130">System.object</span><span class="sxs-lookup"><span data-stu-id="0b780-130">System.String</span></span>

## <span data-ttu-id="0b780-131">輸出</span><span class="sxs-lookup"><span data-stu-id="0b780-131">OUTPUTS</span></span>

### <span data-ttu-id="0b780-132">PSContainerRegistryWebhookEvent 中的 ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0b780-132">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhookEvent</span></span>

## <span data-ttu-id="0b780-133">筆記</span><span class="sxs-lookup"><span data-stu-id="0b780-133">NOTES</span></span>

## <span data-ttu-id="0b780-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="0b780-134">RELATED LINKS</span></span>

[<span data-ttu-id="0b780-135">新-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="0b780-135">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="0b780-136">AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="0b780-136">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="0b780-137">更新-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="0b780-137">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="0b780-138">移除-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="0b780-138">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)

[<span data-ttu-id="0b780-139">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="0b780-139">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)
