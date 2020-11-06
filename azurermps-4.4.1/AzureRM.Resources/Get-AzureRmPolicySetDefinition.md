---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicySetDefinition.md
ms.openlocfilehash: 5fba45e50076952a0a2e11e2e5541ab9546d3bc6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452424"
---
# <span data-ttu-id="9eeb2-101">Get-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="9eeb2-101">Get-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="9eeb2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9eeb2-102">SYNOPSIS</span></span>
<span data-ttu-id="9eeb2-103">取得原則集定義。</span><span class="sxs-lookup"><span data-stu-id="9eeb2-103">Gets policy set definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9eeb2-104">句法</span><span class="sxs-lookup"><span data-stu-id="9eeb2-104">SYNTAX</span></span>

### <span data-ttu-id="9eeb2-105">已設定所有策略集定義參數的清單。</span><span class="sxs-lookup"><span data-stu-id="9eeb2-105">The list all policy set definitions parameter set.</span></span> <span data-ttu-id="9eeb2-106"> (預設) </span><span class="sxs-lookup"><span data-stu-id="9eeb2-106">(Default)</span></span>
```
Get-AzureRmPolicySetDefinition [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9eeb2-107">已設定原則集定義名稱參數。</span><span class="sxs-lookup"><span data-stu-id="9eeb2-107">The policy set definition name parameter set.</span></span>
```
Get-AzureRmPolicySetDefinition -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9eeb2-108">已設定原則集定義識別碼參數。</span><span class="sxs-lookup"><span data-stu-id="9eeb2-108">The policy set definition Id parameter set.</span></span>
```
Get-AzureRmPolicySetDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9eeb2-109">說明</span><span class="sxs-lookup"><span data-stu-id="9eeb2-109">DESCRIPTION</span></span>
<span data-ttu-id="9eeb2-110">**AzureRmPolicySetDefinition** Cmdlet 會取得所有原則集定義，或由名稱或 ID 識別的特定原則集定義。</span><span class="sxs-lookup"><span data-stu-id="9eeb2-110">The **Get-AzureRmPolicySetDefinition** cmdlet gets all the policy set definitions or a specific policy set definition identified by name or ID.</span></span>

## <span data-ttu-id="9eeb2-111">示例</span><span class="sxs-lookup"><span data-stu-id="9eeb2-111">EXAMPLES</span></span>

### <span data-ttu-id="9eeb2-112">範例1：取得所有原則集定義</span><span class="sxs-lookup"><span data-stu-id="9eeb2-112">Example 1: Get all policy set definition</span></span>
```
PS C:\>Get-AzureRmPolicySetDefinition
```

<span data-ttu-id="9eeb2-113">這個命令會取得所有原則集定義。</span><span class="sxs-lookup"><span data-stu-id="9eeb2-113">This command gets all the policy set definitions.</span></span>

### <span data-ttu-id="9eeb2-114">範例2：依名稱取得原則集定義</span><span class="sxs-lookup"><span data-stu-id="9eeb2-114">Example 2: Get policy set definition by name</span></span>
```
PS C:\>Get-AzureRmPolicySetDefinition -Name "VMPolicyDefinition"
```

<span data-ttu-id="9eeb2-115">這個命令會取得名為 VMPolicyDefinition 的原則集定義。</span><span class="sxs-lookup"><span data-stu-id="9eeb2-115">This command gets the policy set definition named VMPolicyDefinition.</span></span>

## <span data-ttu-id="9eeb2-116">參數</span><span class="sxs-lookup"><span data-stu-id="9eeb2-116">PARAMETERS</span></span>

### <span data-ttu-id="9eeb2-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9eeb2-117">-ApiVersion</span></span>
<span data-ttu-id="9eeb2-118">設定時，會指出要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="9eeb2-118">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="9eeb2-119">如果未指定，API 版本會自動決定為最新的可用。</span><span class="sxs-lookup"><span data-stu-id="9eeb2-119">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="9eeb2-120">-識別碼</span><span class="sxs-lookup"><span data-stu-id="9eeb2-120">-Id</span></span>
<span data-ttu-id="9eeb2-121">完全限定的原則集定義識別碼，包括訂閱。</span><span class="sxs-lookup"><span data-stu-id="9eeb2-121">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="9eeb2-122">例如/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="9eeb2-122">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The policy set definition Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9eeb2-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="9eeb2-123">-Name</span></span>
<span data-ttu-id="9eeb2-124">原則集定義名稱。</span><span class="sxs-lookup"><span data-stu-id="9eeb2-124">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy set definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9eeb2-125">-預先</span><span class="sxs-lookup"><span data-stu-id="9eeb2-125">-Pre</span></span>
<span data-ttu-id="9eeb2-126">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="9eeb2-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="9eeb2-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9eeb2-127">-DefaultProfile</span></span>
<span data-ttu-id="9eeb2-128">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9eeb2-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9eeb2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9eeb2-129">CommonParameters</span></span>
<span data-ttu-id="9eeb2-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9eeb2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9eeb2-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9eeb2-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9eeb2-132">輸入</span><span class="sxs-lookup"><span data-stu-id="9eeb2-132">INPUTS</span></span>

### <span data-ttu-id="9eeb2-133">System.object</span><span class="sxs-lookup"><span data-stu-id="9eeb2-133">System.String</span></span>

## <span data-ttu-id="9eeb2-134">輸出</span><span class="sxs-lookup"><span data-stu-id="9eeb2-134">OUTPUTS</span></span>

### <span data-ttu-id="9eeb2-135">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="9eeb2-135">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="9eeb2-136">筆記</span><span class="sxs-lookup"><span data-stu-id="9eeb2-136">NOTES</span></span>

## <span data-ttu-id="9eeb2-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="9eeb2-137">RELATED LINKS</span></span>

