---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/get-azcommunicationservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Get-AzCommunicationServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Get-AzCommunicationServiceKey.md
ms.openlocfilehash: e4a16b69e5919684b40d5b9f7fd4e97465d3565e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98446540"
---
# <span data-ttu-id="3ab18-101">Get-AzCommunicationServiceKey</span><span class="sxs-lookup"><span data-stu-id="3ab18-101">Get-AzCommunicationServiceKey</span></span>

## <span data-ttu-id="3ab18-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3ab18-102">SYNOPSIS</span></span>
<span data-ttu-id="3ab18-103">取得 CommunicationService 資源的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="3ab18-103">Get the access keys of the CommunicationService resource.</span></span>

## <span data-ttu-id="3ab18-104">句法</span><span class="sxs-lookup"><span data-stu-id="3ab18-104">SYNTAX</span></span>

```
Get-AzCommunicationServiceKey -CommunicationServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3ab18-105">說明</span><span class="sxs-lookup"><span data-stu-id="3ab18-105">DESCRIPTION</span></span>
<span data-ttu-id="3ab18-106">取得 CommunicationService 資源的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="3ab18-106">Get the access keys of the CommunicationService resource.</span></span>

## <span data-ttu-id="3ab18-107">示例</span><span class="sxs-lookup"><span data-stu-id="3ab18-107">EXAMPLES</span></span>

### <span data-ttu-id="3ab18-108">範例1：提取指定通訊服務的金鑰</span><span class="sxs-lookup"><span data-stu-id="3ab18-108">Example 1: Fetch the Key for the specified Communcation service</span></span>
```powershell
PS C:\> Get-AzCommunicationServiceKey -CommunicationServiceName ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1

PrimaryConnectionString              PrimaryKey            SecondaryConnectionString               SecondaryKey
-----------------------              ----------            -----------------------                 ----------
endpoint=<example-primary-endpoint>  <example-primarykey>  endpoint=<example-secondary-endpoint>   <example-secondarykey>
```

<span data-ttu-id="3ab18-109">顯示指定通訊服務的 ConnectionString 和鍵。</span><span class="sxs-lookup"><span data-stu-id="3ab18-109">Displays the ConnectionString and Key for the specified Communcation service.</span></span>

## <span data-ttu-id="3ab18-110">參數</span><span class="sxs-lookup"><span data-stu-id="3ab18-110">PARAMETERS</span></span>

### <span data-ttu-id="3ab18-111">-CommunicationServiceName</span><span class="sxs-lookup"><span data-stu-id="3ab18-111">-CommunicationServiceName</span></span>
<span data-ttu-id="3ab18-112">CommunicationService 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="3ab18-112">The name of the CommunicationService resource.</span></span>

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

### <span data-ttu-id="3ab18-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ab18-113">-DefaultProfile</span></span>
<span data-ttu-id="3ab18-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3ab18-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ab18-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ab18-115">-ResourceGroupName</span></span>
<span data-ttu-id="3ab18-116">包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3ab18-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="3ab18-117">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="3ab18-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="3ab18-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3ab18-118">-SubscriptionId</span></span>
<span data-ttu-id="3ab18-119">取得唯一識別 Microsoft Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="3ab18-119">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="3ab18-120">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="3ab18-120">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3ab18-121">-確認</span><span class="sxs-lookup"><span data-stu-id="3ab18-121">-Confirm</span></span>
<span data-ttu-id="3ab18-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3ab18-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ab18-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ab18-123">-WhatIf</span></span>
<span data-ttu-id="3ab18-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3ab18-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ab18-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3ab18-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ab18-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ab18-126">CommonParameters</span></span>
<span data-ttu-id="3ab18-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3ab18-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ab18-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3ab18-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ab18-129">輸入</span><span class="sxs-lookup"><span data-stu-id="3ab18-129">INPUTS</span></span>

## <span data-ttu-id="3ab18-130">輸出</span><span class="sxs-lookup"><span data-stu-id="3ab18-130">OUTPUTS</span></span>

### <span data-ttu-id="3ab18-131">ICommunicationServiceKeys 中的 Api20200820Preview （）。</span><span class="sxs-lookup"><span data-stu-id="3ab18-131">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceKeys</span></span>

## <span data-ttu-id="3ab18-132">筆記</span><span class="sxs-lookup"><span data-stu-id="3ab18-132">NOTES</span></span>

<span data-ttu-id="3ab18-133">別名</span><span class="sxs-lookup"><span data-stu-id="3ab18-133">ALIASES</span></span>

## <span data-ttu-id="3ab18-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="3ab18-134">RELATED LINKS</span></span>

