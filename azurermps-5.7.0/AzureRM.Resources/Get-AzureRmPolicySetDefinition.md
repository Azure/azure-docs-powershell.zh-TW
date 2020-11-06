---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicySetDefinition.md
ms.openlocfilehash: 694f2ef459b50648e934e4ea0e434fe218d4b1f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453064"
---
# <span data-ttu-id="1c01a-101">Get-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="1c01a-101">Get-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="1c01a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1c01a-102">SYNOPSIS</span></span>
<span data-ttu-id="1c01a-103">取得原則集定義。</span><span class="sxs-lookup"><span data-stu-id="1c01a-103">Gets policy set definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c01a-104">句法</span><span class="sxs-lookup"><span data-stu-id="1c01a-104">SYNTAX</span></span>

### <span data-ttu-id="1c01a-105">GetBySubscription (預設) </span><span class="sxs-lookup"><span data-stu-id="1c01a-105">GetBySubscription (Default)</span></span>
```
Get-AzureRmPolicySetDefinition [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1c01a-106">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1c01a-106">GetByNameAndResourceGroup</span></span>
```
Get-AzureRmPolicySetDefinition -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c01a-107">GetById</span><span class="sxs-lookup"><span data-stu-id="1c01a-107">GetById</span></span>
```
Get-AzureRmPolicySetDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c01a-108">說明</span><span class="sxs-lookup"><span data-stu-id="1c01a-108">DESCRIPTION</span></span>
<span data-ttu-id="1c01a-109">**AzureRmPolicySetDefinition** Cmdlet 會取得所有原則集定義，或由名稱或 ID 識別的特定原則集定義。</span><span class="sxs-lookup"><span data-stu-id="1c01a-109">The **Get-AzureRmPolicySetDefinition** cmdlet gets all the policy set definitions or a specific policy set definition identified by name or ID.</span></span>

## <span data-ttu-id="1c01a-110">示例</span><span class="sxs-lookup"><span data-stu-id="1c01a-110">EXAMPLES</span></span>

### <span data-ttu-id="1c01a-111">範例1：取得所有原則集定義</span><span class="sxs-lookup"><span data-stu-id="1c01a-111">Example 1: Get all policy set definition</span></span>
```
PS C:\>Get-AzureRmPolicySetDefinition
```

<span data-ttu-id="1c01a-112">這個命令會取得所有原則集定義。</span><span class="sxs-lookup"><span data-stu-id="1c01a-112">This command gets all the policy set definitions.</span></span>

### <span data-ttu-id="1c01a-113">範例2：依名稱取得原則集定義</span><span class="sxs-lookup"><span data-stu-id="1c01a-113">Example 2: Get policy set definition by name</span></span>
```
PS C:\>Get-AzureRmPolicySetDefinition -Name "VMPolicyDefinition"
```

<span data-ttu-id="1c01a-114">這個命令會取得名為 VMPolicyDefinition 的原則集定義。</span><span class="sxs-lookup"><span data-stu-id="1c01a-114">This command gets the policy set definition named VMPolicyDefinition.</span></span>

## <span data-ttu-id="1c01a-115">參數</span><span class="sxs-lookup"><span data-stu-id="1c01a-115">PARAMETERS</span></span>

### <span data-ttu-id="1c01a-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="1c01a-116">-ApiVersion</span></span>
<span data-ttu-id="1c01a-117">設定時，會指出要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="1c01a-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="1c01a-118">如果未指定，API 版本會自動決定為最新的可用。</span><span class="sxs-lookup"><span data-stu-id="1c01a-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="1c01a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c01a-119">-DefaultProfile</span></span>
<span data-ttu-id="1c01a-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="1c01a-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1c01a-121">-識別碼</span><span class="sxs-lookup"><span data-stu-id="1c01a-121">-Id</span></span>
<span data-ttu-id="1c01a-122">完全限定的原則集定義識別碼，包括訂閱。</span><span class="sxs-lookup"><span data-stu-id="1c01a-122">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="1c01a-123">例如/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="1c01a-123">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: String
Parameter Sets: GetById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c01a-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="1c01a-124">-Name</span></span>
<span data-ttu-id="1c01a-125">原則集定義名稱。</span><span class="sxs-lookup"><span data-stu-id="1c01a-125">The policy set definition name.</span></span>

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

### <span data-ttu-id="1c01a-126">-預先</span><span class="sxs-lookup"><span data-stu-id="1c01a-126">-Pre</span></span>
<span data-ttu-id="1c01a-127">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="1c01a-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="1c01a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c01a-128">CommonParameters</span></span>
<span data-ttu-id="1c01a-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1c01a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c01a-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1c01a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c01a-131">輸入</span><span class="sxs-lookup"><span data-stu-id="1c01a-131">INPUTS</span></span>

### <span data-ttu-id="1c01a-132">System.object</span><span class="sxs-lookup"><span data-stu-id="1c01a-132">System.String</span></span>

## <span data-ttu-id="1c01a-133">輸出</span><span class="sxs-lookup"><span data-stu-id="1c01a-133">OUTPUTS</span></span>

### <span data-ttu-id="1c01a-134">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="1c01a-134">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="1c01a-135">筆記</span><span class="sxs-lookup"><span data-stu-id="1c01a-135">NOTES</span></span>

## <span data-ttu-id="1c01a-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="1c01a-136">RELATED LINKS</span></span>
