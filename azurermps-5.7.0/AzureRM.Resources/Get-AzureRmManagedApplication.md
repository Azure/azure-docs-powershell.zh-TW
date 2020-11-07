---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagedApplication.md
ms.openlocfilehash: 3dd86c186d05ce59f237be51b8e059e800c47a84
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624680"
---
# <span data-ttu-id="d89d8-101">Get-AzureRmManagedApplication</span><span class="sxs-lookup"><span data-stu-id="d89d8-101">Get-AzureRmManagedApplication</span></span>

## <span data-ttu-id="d89d8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d89d8-102">SYNOPSIS</span></span>
<span data-ttu-id="d89d8-103">取得受管理的應用程式</span><span class="sxs-lookup"><span data-stu-id="d89d8-103">Gets managed applications</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d89d8-104">句法</span><span class="sxs-lookup"><span data-stu-id="d89d8-104">SYNTAX</span></span>

### <span data-ttu-id="d89d8-105">GetBySubscription (預設) </span><span class="sxs-lookup"><span data-stu-id="d89d8-105">GetBySubscription (Default)</span></span>
```
Get-AzureRmManagedApplication [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d89d8-106">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d89d8-106">GetByNameAndResourceGroup</span></span>
```
Get-AzureRmManagedApplication [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d89d8-107">GetById</span><span class="sxs-lookup"><span data-stu-id="d89d8-107">GetById</span></span>
```
Get-AzureRmManagedApplication -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d89d8-108">說明</span><span class="sxs-lookup"><span data-stu-id="d89d8-108">DESCRIPTION</span></span>
<span data-ttu-id="d89d8-109">AzureRmManagedApplication Cmdlet 會取得受管理 **的** 應用程式</span><span class="sxs-lookup"><span data-stu-id="d89d8-109">The **Get-AzureRmManagedApplication** cmdlet gets managed applications</span></span>

## <span data-ttu-id="d89d8-110">示例</span><span class="sxs-lookup"><span data-stu-id="d89d8-110">EXAMPLES</span></span>

### <span data-ttu-id="d89d8-111">範例1：取得資源群組下的所有受管理的應用程式</span><span class="sxs-lookup"><span data-stu-id="d89d8-111">Example 1: Get all managed applications under a resource group</span></span>
```
PS C:\>Get-AzureRmManagedApplication -ResourceGroupName "MyRG"
```

<span data-ttu-id="d89d8-112">這個命令會在 [資源] 群組的 [MyRG] 下取得受管理的應用程式</span><span class="sxs-lookup"><span data-stu-id="d89d8-112">This command gets managed applications under resource group "MyRG"</span></span>

### <span data-ttu-id="d89d8-113">範例2：取得所有受管理的應用程式</span><span class="sxs-lookup"><span data-stu-id="d89d8-113">Example 2: Get all managed applications</span></span>
```
PS C:\>Get-AzureRmManagedApplication
```

<span data-ttu-id="d89d8-114">這個命令會在目前的訂閱中取得所有受管理的應用程式</span><span class="sxs-lookup"><span data-stu-id="d89d8-114">This command get all managed applications under the current subscription</span></span>

## <span data-ttu-id="d89d8-115">參數</span><span class="sxs-lookup"><span data-stu-id="d89d8-115">PARAMETERS</span></span>

### <span data-ttu-id="d89d8-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d89d8-116">-ApiVersion</span></span>
<span data-ttu-id="d89d8-117">設定時，會指出要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="d89d8-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="d89d8-118">如果未指定，API 版本會自動決定為最新的可用。</span><span class="sxs-lookup"><span data-stu-id="d89d8-118">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d89d8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d89d8-119">-DefaultProfile</span></span>
<span data-ttu-id="d89d8-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d89d8-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d89d8-121">-識別碼</span><span class="sxs-lookup"><span data-stu-id="d89d8-121">-Id</span></span>
<span data-ttu-id="d89d8-122">完全限定的管理應用程式識別碼，包括訂閱。</span><span class="sxs-lookup"><span data-stu-id="d89d8-122">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="d89d8-123">例如/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="d89d8-123">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: String
Parameter Sets: GetById
Aliases: ResourceId, ManagedApplicationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d89d8-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="d89d8-124">-Name</span></span>
<span data-ttu-id="d89d8-125">受管理的應用程式名稱。</span><span class="sxs-lookup"><span data-stu-id="d89d8-125">The managed application name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d89d8-126">-預先</span><span class="sxs-lookup"><span data-stu-id="d89d8-126">-Pre</span></span>
<span data-ttu-id="d89d8-127">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="d89d8-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="d89d8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d89d8-128">-ResourceGroupName</span></span>
<span data-ttu-id="d89d8-129">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d89d8-129">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d89d8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d89d8-130">CommonParameters</span></span>
<span data-ttu-id="d89d8-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d89d8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d89d8-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d89d8-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d89d8-133">輸入</span><span class="sxs-lookup"><span data-stu-id="d89d8-133">INPUTS</span></span>

### <span data-ttu-id="d89d8-134">System.object</span><span class="sxs-lookup"><span data-stu-id="d89d8-134">System.String</span></span>

## <span data-ttu-id="d89d8-135">輸出</span><span class="sxs-lookup"><span data-stu-id="d89d8-135">OUTPUTS</span></span>

### <span data-ttu-id="d89d8-136">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="d89d8-136">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="d89d8-137">筆記</span><span class="sxs-lookup"><span data-stu-id="d89d8-137">NOTES</span></span>

## <span data-ttu-id="d89d8-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="d89d8-138">RELATED LINKS</span></span>
