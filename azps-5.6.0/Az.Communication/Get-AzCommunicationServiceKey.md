---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/powershell/module/az.communication/get-azcommunicationservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Get-AzCommunicationServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Get-AzCommunicationServiceKey.md
ms.openlocfilehash: 82e5f6ced22b17c8966afbd5bc57324ab2069d1c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912094"
---
# <span data-ttu-id="3d3e8-101">Get-AzCommunicationServiceKey</span><span class="sxs-lookup"><span data-stu-id="3d3e8-101">Get-AzCommunicationServiceKey</span></span>

## <span data-ttu-id="3d3e8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3d3e8-102">SYNOPSIS</span></span>
<span data-ttu-id="3d3e8-103">取得 CommunicationService 資源的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="3d3e8-103">Get the access keys of the CommunicationService resource.</span></span>

## <span data-ttu-id="3d3e8-104">語法</span><span class="sxs-lookup"><span data-stu-id="3d3e8-104">SYNTAX</span></span>

```
Get-AzCommunicationServiceKey -CommunicationServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3d3e8-105">描述</span><span class="sxs-lookup"><span data-stu-id="3d3e8-105">DESCRIPTION</span></span>
<span data-ttu-id="3d3e8-106">取得 CommunicationService 資源的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="3d3e8-106">Get the access keys of the CommunicationService resource.</span></span>

## <span data-ttu-id="3d3e8-107">例子</span><span class="sxs-lookup"><span data-stu-id="3d3e8-107">EXAMPLES</span></span>

### <span data-ttu-id="3d3e8-108">範例 1：為指定的通訊服務抓取金鑰</span><span class="sxs-lookup"><span data-stu-id="3d3e8-108">Example 1: Fetch the Key for the specified Communcation service</span></span>
```powershell
PS C:\> Get-AzCommunicationServiceKey -CommunicationServiceName ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1

PrimaryConnectionString              PrimaryKey            SecondaryConnectionString               SecondaryKey
-----------------------              ----------            -----------------------                 ----------
endpoint=<example-primary-endpoint>  <example-primarykey>  endpoint=<example-secondary-endpoint>   <example-secondarykey>
```

<span data-ttu-id="3d3e8-109">顯示指定通訊服務的 ConnectionString 和 Key。</span><span class="sxs-lookup"><span data-stu-id="3d3e8-109">Displays the ConnectionString and Key for the specified Communcation service.</span></span>

## <span data-ttu-id="3d3e8-110">參數</span><span class="sxs-lookup"><span data-stu-id="3d3e8-110">PARAMETERS</span></span>

### <span data-ttu-id="3d3e8-111">-CommunicationServiceName</span><span class="sxs-lookup"><span data-stu-id="3d3e8-111">-CommunicationServiceName</span></span>
<span data-ttu-id="3d3e8-112">CommunicationService 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="3d3e8-112">The name of the CommunicationService resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d3e8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d3e8-113">-DefaultProfile</span></span>
<span data-ttu-id="3d3e8-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3d3e8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d3e8-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d3e8-115">-ResourceGroupName</span></span>
<span data-ttu-id="3d3e8-116">包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="3d3e8-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="3d3e8-117">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="3d3e8-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d3e8-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3d3e8-118">-SubscriptionId</span></span>
<span data-ttu-id="3d3e8-119">獲得可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="3d3e8-119">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="3d3e8-120">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="3d3e8-120">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d3e8-121">-確認</span><span class="sxs-lookup"><span data-stu-id="3d3e8-121">-Confirm</span></span>
<span data-ttu-id="3d3e8-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="3d3e8-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d3e8-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d3e8-123">-WhatIf</span></span>
<span data-ttu-id="3d3e8-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3d3e8-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d3e8-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3d3e8-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d3e8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d3e8-126">CommonParameters</span></span>
<span data-ttu-id="3d3e8-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3d3e8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d3e8-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3d3e8-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d3e8-129">輸入</span><span class="sxs-lookup"><span data-stu-id="3d3e8-129">INPUTS</span></span>

## <span data-ttu-id="3d3e8-130">輸出</span><span class="sxs-lookup"><span data-stu-id="3d3e8-130">OUTPUTS</span></span>

### <span data-ttu-id="3d3e8-131">Microsoft.Azure.PowerShell.Cmdlets.Communication.models.Api20200820Preview.ICommunicationServiceKeys</span><span class="sxs-lookup"><span data-stu-id="3d3e8-131">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceKeys</span></span>

## <span data-ttu-id="3d3e8-132">筆記</span><span class="sxs-lookup"><span data-stu-id="3d3e8-132">NOTES</span></span>

<span data-ttu-id="3d3e8-133">別名</span><span class="sxs-lookup"><span data-stu-id="3d3e8-133">ALIASES</span></span>

## <span data-ttu-id="3d3e8-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="3d3e8-134">RELATED LINKS</span></span>

