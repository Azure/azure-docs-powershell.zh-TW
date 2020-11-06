---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagedApplication.md
ms.openlocfilehash: 953a810585550ec8895fc9306f78633beb4846a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446679"
---
# <span data-ttu-id="a143f-101">Get-AzureRmManagedApplication</span><span class="sxs-lookup"><span data-stu-id="a143f-101">Get-AzureRmManagedApplication</span></span>

## <span data-ttu-id="a143f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a143f-102">SYNOPSIS</span></span>
<span data-ttu-id="a143f-103">取得受管理的應用程式</span><span class="sxs-lookup"><span data-stu-id="a143f-103">Gets managed applications</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a143f-104">句法</span><span class="sxs-lookup"><span data-stu-id="a143f-104">SYNTAX</span></span>

### <span data-ttu-id="a143f-105">清單所有受管理的應用程式參數集。</span><span class="sxs-lookup"><span data-stu-id="a143f-105">The list all managed applications parameter set.</span></span> <span data-ttu-id="a143f-106"> (預設) </span><span class="sxs-lookup"><span data-stu-id="a143f-106">(Default)</span></span>
```
Get-AzureRmManagedApplication [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a143f-107">已設定受管理的應用程式名稱參數。</span><span class="sxs-lookup"><span data-stu-id="a143f-107">The managed application name parameter set.</span></span>
```
Get-AzureRmManagedApplication [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a143f-108">已設定受管理的應用程式識別碼參數。</span><span class="sxs-lookup"><span data-stu-id="a143f-108">The managed application Id parameter set.</span></span>
```
Get-AzureRmManagedApplication -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a143f-109">說明</span><span class="sxs-lookup"><span data-stu-id="a143f-109">DESCRIPTION</span></span>
<span data-ttu-id="a143f-110">AzureRmManagedApplication Cmdlet 會取得受管理 **的** 應用程式</span><span class="sxs-lookup"><span data-stu-id="a143f-110">The **Get-AzureRmManagedApplication** cmdlet gets managed applications</span></span>

## <span data-ttu-id="a143f-111">示例</span><span class="sxs-lookup"><span data-stu-id="a143f-111">EXAMPLES</span></span>

### <span data-ttu-id="a143f-112">範例1：取得資源群組下的所有受管理的應用程式</span><span class="sxs-lookup"><span data-stu-id="a143f-112">Example 1: Get all managed applications under a resource group</span></span>
```
PS C:\>Get-AzureRmManagedApplication -ResourceGroupName "MyRG"
```

<span data-ttu-id="a143f-113">這個命令會在 [資源] 群組的 [MyRG] 下取得受管理的應用程式</span><span class="sxs-lookup"><span data-stu-id="a143f-113">This command gets managed applications under resource group "MyRG"</span></span>

### <span data-ttu-id="a143f-114">範例2：取得所有受管理的應用程式</span><span class="sxs-lookup"><span data-stu-id="a143f-114">Example 2: Get all managed applications</span></span>
```
PS C:\>Get-AzureRmManagedApplication
```

<span data-ttu-id="a143f-115">這個命令會在目前的訂閱中取得所有受管理的應用程式</span><span class="sxs-lookup"><span data-stu-id="a143f-115">This command get all managed applications under the current subscription</span></span>

## <span data-ttu-id="a143f-116">參數</span><span class="sxs-lookup"><span data-stu-id="a143f-116">PARAMETERS</span></span>

### <span data-ttu-id="a143f-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a143f-117">-ApiVersion</span></span>
<span data-ttu-id="a143f-118">設定時，會指出要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="a143f-118">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="a143f-119">如果未指定，API 版本會自動決定為最新的可用。</span><span class="sxs-lookup"><span data-stu-id="a143f-119">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="a143f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a143f-120">-DefaultProfile</span></span>
<span data-ttu-id="a143f-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a143f-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a143f-122">-識別碼</span><span class="sxs-lookup"><span data-stu-id="a143f-122">-Id</span></span>
<span data-ttu-id="a143f-123">完全限定的管理應用程式識別碼，包括訂閱。</span><span class="sxs-lookup"><span data-stu-id="a143f-123">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="a143f-124">例如/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="a143f-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application Id parameter set.
Aliases: ResourceId, ManagedApplicationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a143f-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="a143f-125">-Name</span></span>
<span data-ttu-id="a143f-126">受管理的應用程式名稱。</span><span class="sxs-lookup"><span data-stu-id="a143f-126">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application name parameter set.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a143f-127">-預先</span><span class="sxs-lookup"><span data-stu-id="a143f-127">-Pre</span></span>
<span data-ttu-id="a143f-128">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="a143f-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="a143f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a143f-129">-ResourceGroupName</span></span>
<span data-ttu-id="a143f-130">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a143f-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a143f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a143f-131">CommonParameters</span></span>
<span data-ttu-id="a143f-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a143f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a143f-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a143f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a143f-134">輸入</span><span class="sxs-lookup"><span data-stu-id="a143f-134">INPUTS</span></span>

### <span data-ttu-id="a143f-135">System.object</span><span class="sxs-lookup"><span data-stu-id="a143f-135">System.String</span></span>

## <span data-ttu-id="a143f-136">輸出</span><span class="sxs-lookup"><span data-stu-id="a143f-136">OUTPUTS</span></span>

### <span data-ttu-id="a143f-137">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="a143f-137">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="a143f-138">筆記</span><span class="sxs-lookup"><span data-stu-id="a143f-138">NOTES</span></span>

## <span data-ttu-id="a143f-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="a143f-139">RELATED LINKS</span></span>

