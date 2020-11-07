---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicySetDefinition.md
ms.openlocfilehash: 9c860726993929a6618706037b5c53dff14a68ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625075"
---
# <span data-ttu-id="1f36b-101">New-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="1f36b-101">New-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="1f36b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1f36b-102">SYNOPSIS</span></span>
<span data-ttu-id="1f36b-103">建立原則集定義。</span><span class="sxs-lookup"><span data-stu-id="1f36b-103">Creates a policy set definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f36b-104">句法</span><span class="sxs-lookup"><span data-stu-id="1f36b-104">SYNTAX</span></span>

```
New-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyDefinition <String> [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f36b-105">說明</span><span class="sxs-lookup"><span data-stu-id="1f36b-105">DESCRIPTION</span></span>
<span data-ttu-id="1f36b-106">**新的-AzureRmPolicySetDefinition** Cmdlet 會建立一個策略集定義。</span><span class="sxs-lookup"><span data-stu-id="1f36b-106">The **New-AzureRmPolicySetDefinition** cmdlet creates a policy set definition.</span></span>

## <span data-ttu-id="1f36b-107">示例</span><span class="sxs-lookup"><span data-stu-id="1f36b-107">EXAMPLES</span></span>

### <span data-ttu-id="1f36b-108">範例1：使用原則集檔案建立原則集定義</span><span class="sxs-lookup"><span data-stu-id="1f36b-108">Example 1: Create a policy set definition by using a policy set file</span></span>
```
PS C:\>New-AzureRmPolicySetDefinition -Name "VMPolicyDefinition" -PolicyDefinition C:\VMPolicySet.json
```

<span data-ttu-id="1f36b-109">這個命令會建立一個名為 VMPolicyDefinition 的原則集定義，其中包含 C:\VMPolicy.json 中指定的原則定義。</span><span class="sxs-lookup"><span data-stu-id="1f36b-109">This command creates a policy set definition named VMPolicyDefinition that contains the policy definitions specified in C:\VMPolicy.json.</span></span>

## <span data-ttu-id="1f36b-110">參數</span><span class="sxs-lookup"><span data-stu-id="1f36b-110">PARAMETERS</span></span>

### <span data-ttu-id="1f36b-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="1f36b-111">-ApiVersion</span></span>
<span data-ttu-id="1f36b-112">設定時，會指出要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="1f36b-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="1f36b-113">如果未指定，API 版本會自動決定為最新的可用。</span><span class="sxs-lookup"><span data-stu-id="1f36b-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="1f36b-114">-描述</span><span class="sxs-lookup"><span data-stu-id="1f36b-114">-Description</span></span>
<span data-ttu-id="1f36b-115">原則集定義的描述。</span><span class="sxs-lookup"><span data-stu-id="1f36b-115">The description for policy set definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f36b-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="1f36b-116">-DisplayName</span></span>
<span data-ttu-id="1f36b-117">原則集定義的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="1f36b-117">The display name for policy set definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f36b-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="1f36b-118">-Name</span></span>
<span data-ttu-id="1f36b-119">原則集定義名稱。</span><span class="sxs-lookup"><span data-stu-id="1f36b-119">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f36b-120">-參數</span><span class="sxs-lookup"><span data-stu-id="1f36b-120">-Parameter</span></span>
<span data-ttu-id="1f36b-121">原則集定義的參數宣告。</span><span class="sxs-lookup"><span data-stu-id="1f36b-121">The parameters declaration for policy set definition.</span></span>
<span data-ttu-id="1f36b-122">這可以是包含參數宣告之檔案名的路徑，或是參數宣告（字串）。</span><span class="sxs-lookup"><span data-stu-id="1f36b-122">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f36b-123">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1f36b-123">-PolicyDefinition</span></span>
<span data-ttu-id="1f36b-124">原則集定義。</span><span class="sxs-lookup"><span data-stu-id="1f36b-124">The policy set definition.</span></span> <span data-ttu-id="1f36b-125">這可以是包含原則定義的檔案名路徑，或原則集定義（字串）。</span><span class="sxs-lookup"><span data-stu-id="1f36b-125">This can either be a path to a file name containing the policy definitions, or the policy set definition as string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f36b-126">-預先</span><span class="sxs-lookup"><span data-stu-id="1f36b-126">-Pre</span></span>
<span data-ttu-id="1f36b-127">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="1f36b-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="1f36b-128">-確認</span><span class="sxs-lookup"><span data-stu-id="1f36b-128">-Confirm</span></span>
<span data-ttu-id="1f36b-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1f36b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f36b-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f36b-130">-DefaultProfile</span></span>
<span data-ttu-id="1f36b-131">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1f36b-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f36b-132">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="1f36b-132">-Metadata</span></span>
<span data-ttu-id="1f36b-133">原則集定義的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="1f36b-133">The metadata for policy set definition.</span></span> <span data-ttu-id="1f36b-134">這可以是包含中繼資料之檔案名的路徑，或以字串形式的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="1f36b-134">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f36b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f36b-135">-WhatIf</span></span>
<span data-ttu-id="1f36b-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1f36b-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1f36b-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1f36b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f36b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f36b-138">CommonParameters</span></span>
<span data-ttu-id="1f36b-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1f36b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f36b-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1f36b-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f36b-141">輸入</span><span class="sxs-lookup"><span data-stu-id="1f36b-141">INPUTS</span></span>

### <span data-ttu-id="1f36b-142">System.object</span><span class="sxs-lookup"><span data-stu-id="1f36b-142">System.String</span></span>

## <span data-ttu-id="1f36b-143">輸出</span><span class="sxs-lookup"><span data-stu-id="1f36b-143">OUTPUTS</span></span>

### <span data-ttu-id="1f36b-144">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="1f36b-144">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="1f36b-145">筆記</span><span class="sxs-lookup"><span data-stu-id="1f36b-145">NOTES</span></span>

## <span data-ttu-id="1f36b-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="1f36b-146">RELATED LINKS</span></span>

