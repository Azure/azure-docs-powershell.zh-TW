---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplication.md
ms.openlocfilehash: e0577342a839424d9a45a91b6c9289a72fe9df12
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98273871"
---
# <span data-ttu-id="70311-101">Get-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="70311-101">Get-AzManagedApplication</span></span>

## <span data-ttu-id="70311-102">摘要</span><span class="sxs-lookup"><span data-stu-id="70311-102">SYNOPSIS</span></span>
<span data-ttu-id="70311-103">取得受管理的應用程式</span><span class="sxs-lookup"><span data-stu-id="70311-103">Gets managed applications</span></span>

## <span data-ttu-id="70311-104">句法</span><span class="sxs-lookup"><span data-stu-id="70311-104">SYNTAX</span></span>

### <span data-ttu-id="70311-105">GetBySubscription (預設) </span><span class="sxs-lookup"><span data-stu-id="70311-105">GetBySubscription (Default)</span></span>
```
Get-AzManagedApplication [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="70311-106">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="70311-106">GetByNameAndResourceGroup</span></span>
```
Get-AzManagedApplication [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="70311-107">GetById</span><span class="sxs-lookup"><span data-stu-id="70311-107">GetById</span></span>
```
Get-AzManagedApplication -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="70311-108">說明</span><span class="sxs-lookup"><span data-stu-id="70311-108">DESCRIPTION</span></span>
<span data-ttu-id="70311-109">AzManagedApplication Cmdlet 會取得受管理 **的** 應用程式</span><span class="sxs-lookup"><span data-stu-id="70311-109">The **Get-AzManagedApplication** cmdlet gets managed applications</span></span>

## <span data-ttu-id="70311-110">示例</span><span class="sxs-lookup"><span data-stu-id="70311-110">EXAMPLES</span></span>

### <span data-ttu-id="70311-111">範例1：取得資源群組下的所有受管理的應用程式</span><span class="sxs-lookup"><span data-stu-id="70311-111">Example 1: Get all managed applications under a resource group</span></span>
```
PS C:\>Get-AzManagedApplication -ResourceGroupName "MyRG"
```

<span data-ttu-id="70311-112">這個命令會在 [資源] 群組的 [MyRG] 下取得受管理的應用程式</span><span class="sxs-lookup"><span data-stu-id="70311-112">This command gets managed applications under resource group "MyRG"</span></span>

### <span data-ttu-id="70311-113">範例2：取得所有受管理的應用程式</span><span class="sxs-lookup"><span data-stu-id="70311-113">Example 2: Get all managed applications</span></span>
```
PS C:\>Get-AzManagedApplication
```

<span data-ttu-id="70311-114">這個命令會在目前的訂閱中取得所有受管理的應用程式</span><span class="sxs-lookup"><span data-stu-id="70311-114">This command get all managed applications under the current subscription</span></span>

## <span data-ttu-id="70311-115">參數</span><span class="sxs-lookup"><span data-stu-id="70311-115">PARAMETERS</span></span>

### <span data-ttu-id="70311-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="70311-116">-ApiVersion</span></span>
<span data-ttu-id="70311-117">設定時，會指出要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="70311-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="70311-118">如果未指定，API 版本會自動決定為最新的可用。</span><span class="sxs-lookup"><span data-stu-id="70311-118">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70311-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70311-119">-DefaultProfile</span></span>
<span data-ttu-id="70311-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="70311-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70311-121">-識別碼</span><span class="sxs-lookup"><span data-stu-id="70311-121">-Id</span></span>
<span data-ttu-id="70311-122">完全限定的管理應用程式識別碼，包括訂閱。</span><span class="sxs-lookup"><span data-stu-id="70311-122">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="70311-123">例如/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="70311-123">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetById
Aliases: ResourceId, ManagedApplicationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70311-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="70311-124">-Name</span></span>
<span data-ttu-id="70311-125">受管理的應用程式名稱。</span><span class="sxs-lookup"><span data-stu-id="70311-125">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70311-126">-預先</span><span class="sxs-lookup"><span data-stu-id="70311-126">-Pre</span></span>
<span data-ttu-id="70311-127">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="70311-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="70311-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70311-128">-ResourceGroupName</span></span>
<span data-ttu-id="70311-129">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="70311-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70311-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70311-130">CommonParameters</span></span>
<span data-ttu-id="70311-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="70311-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70311-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="70311-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70311-133">輸入</span><span class="sxs-lookup"><span data-stu-id="70311-133">INPUTS</span></span>

### <span data-ttu-id="70311-134">System.object</span><span class="sxs-lookup"><span data-stu-id="70311-134">System.String</span></span>

## <span data-ttu-id="70311-135">輸出</span><span class="sxs-lookup"><span data-stu-id="70311-135">OUTPUTS</span></span>

### <span data-ttu-id="70311-136">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="70311-136">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="70311-137">筆記</span><span class="sxs-lookup"><span data-stu-id="70311-137">NOTES</span></span>

## <span data-ttu-id="70311-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="70311-138">RELATED LINKS</span></span>
