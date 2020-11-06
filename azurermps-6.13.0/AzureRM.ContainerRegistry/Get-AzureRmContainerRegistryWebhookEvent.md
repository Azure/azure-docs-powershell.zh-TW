---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/get-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryWebhookEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryWebhookEvent.md
ms.openlocfilehash: 5e14d1e3f146281ec800914474c5caf3ca3cd47e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93443931"
---
# <span data-ttu-id="c5a6c-101">Get-AzureRmContainerRegistryWebhookEvent</span><span class="sxs-lookup"><span data-stu-id="c5a6c-101">Get-AzureRmContainerRegistryWebhookEvent</span></span>

## <span data-ttu-id="c5a6c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c5a6c-102">SYNOPSIS</span></span>
<span data-ttu-id="c5a6c-103">取得容器註冊 webhook 的事件。</span><span class="sxs-lookup"><span data-stu-id="c5a6c-103">Gets events of a container registry webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5a6c-104">句法</span><span class="sxs-lookup"><span data-stu-id="c5a6c-104">SYNTAX</span></span>

### <span data-ttu-id="c5a6c-105">ListWebhookEventsByNameResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c5a6c-105">ListWebhookEventsByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistryWebhookEvent [-WebhookName] <String> [-ResourceGroupName] <String>
 [-RegistryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5a6c-106">ListWebhookEventsByWebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5a6c-106">ListWebhookEventsByWebhookObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryWebhookEvent -Webhook <PSContainerRegistryWebhook>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5a6c-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5a6c-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmContainerRegistryWebhookEvent -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c5a6c-108">說明</span><span class="sxs-lookup"><span data-stu-id="c5a6c-108">DESCRIPTION</span></span>
<span data-ttu-id="c5a6c-109">Get-AzureRmContainerRegistryWebhookEvent Cmdlet 會列出 webhook 的所有事件。</span><span class="sxs-lookup"><span data-stu-id="c5a6c-109">The Get-AzureRmContainerRegistryWebhookEvent cmdlet lists all the events of a webhook.</span></span>

## <span data-ttu-id="c5a6c-110">示例</span><span class="sxs-lookup"><span data-stu-id="c5a6c-110">EXAMPLES</span></span>

### <span data-ttu-id="c5a6c-111">範例1：取得 webhook 的所有事件。</span><span class="sxs-lookup"><span data-stu-id="c5a6c-111">Example 1: Gets all the events of a webhook.</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryWebhookEvent -ResourceGroupName mattacrtest001 -RegistryName premium001 -Name webhook001

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

<span data-ttu-id="c5a6c-112">取得 webhook 的所有事件。</span><span class="sxs-lookup"><span data-stu-id="c5a6c-112">Gets all the events of a webhook.</span></span>

## <span data-ttu-id="c5a6c-113">參數</span><span class="sxs-lookup"><span data-stu-id="c5a6c-113">PARAMETERS</span></span>

### <span data-ttu-id="c5a6c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5a6c-114">-DefaultProfile</span></span>
<span data-ttu-id="c5a6c-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c5a6c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5a6c-116">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="c5a6c-116">-RegistryName</span></span>
<span data-ttu-id="c5a6c-117">容器登錄名。</span><span class="sxs-lookup"><span data-stu-id="c5a6c-117">Container Registry Name.</span></span>

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

### <span data-ttu-id="c5a6c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5a6c-118">-ResourceGroupName</span></span>
<span data-ttu-id="c5a6c-119">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="c5a6c-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="c5a6c-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c5a6c-120">-ResourceId</span></span>
<span data-ttu-id="c5a6c-121">容器登錄 Webhook 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="c5a6c-121">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="c5a6c-122">-Webhook</span><span class="sxs-lookup"><span data-stu-id="c5a6c-122">-Webhook</span></span>
<span data-ttu-id="c5a6c-123">分枝 Registry 物件。</span><span class="sxs-lookup"><span data-stu-id="c5a6c-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="c5a6c-124">-WebhookName</span><span class="sxs-lookup"><span data-stu-id="c5a6c-124">-WebhookName</span></span>
<span data-ttu-id="c5a6c-125">Webhook 名稱。</span><span class="sxs-lookup"><span data-stu-id="c5a6c-125">Webhook Name.</span></span>

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

### <span data-ttu-id="c5a6c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5a6c-126">CommonParameters</span></span>
<span data-ttu-id="c5a6c-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c5a6c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5a6c-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c5a6c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5a6c-129">輸入</span><span class="sxs-lookup"><span data-stu-id="c5a6c-129">INPUTS</span></span>

### <span data-ttu-id="c5a6c-130">System.object</span><span class="sxs-lookup"><span data-stu-id="c5a6c-130">System.String</span></span>

## <span data-ttu-id="c5a6c-131">輸出</span><span class="sxs-lookup"><span data-stu-id="c5a6c-131">OUTPUTS</span></span>

### <span data-ttu-id="c5a6c-132">PSContainerRegistryWebhookEvent 中的 ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c5a6c-132">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhookEvent</span></span>

## <span data-ttu-id="c5a6c-133">筆記</span><span class="sxs-lookup"><span data-stu-id="c5a6c-133">NOTES</span></span>

## <span data-ttu-id="c5a6c-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="c5a6c-134">RELATED LINKS</span></span>

[<span data-ttu-id="c5a6c-135">新-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="c5a6c-135">New-AzureRmContainerRegistryWebhook</span></span>](New-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="c5a6c-136">AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="c5a6c-136">Get-AzureRmContainerRegistryWebhook</span></span>](Get-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="c5a6c-137">更新-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="c5a6c-137">Update-AzureRmContainerRegistryWebhook</span></span>](Update-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="c5a6c-138">移除-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="c5a6c-138">Remove-AzureRmContainerRegistryWebhook</span></span>](Remove-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="c5a6c-139">Test-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="c5a6c-139">Test-AzureRmContainerRegistryWebhook</span></span>](Test-AzureRmContainerRegistryWebhook.md)

