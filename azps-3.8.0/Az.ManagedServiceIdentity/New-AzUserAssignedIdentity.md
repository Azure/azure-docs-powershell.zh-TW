---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServiceIdentity.dll-Help.xml
Module Name: Az.ManagedServiceIdentity
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/new-azuserassignedidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/New-AzUserAssignedIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/New-AzUserAssignedIdentity.md
ms.openlocfilehash: 1f165177871a2d8b425829dddaef6d1f0298cfb4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965655"
---
# <span data-ttu-id="1e809-101">New-AzUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="1e809-101">New-AzUserAssignedIdentity</span></span>

## <span data-ttu-id="1e809-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1e809-102">SYNOPSIS</span></span>
<span data-ttu-id="1e809-103">建立指派身分識別的新使用者，或更新現有的指派身分識別身分識別的使用者。</span><span class="sxs-lookup"><span data-stu-id="1e809-103">Creates a new User Assigned Identity or updates an existing User Assigned Identity.</span></span>

## <span data-ttu-id="1e809-104">句法</span><span class="sxs-lookup"><span data-stu-id="1e809-104">SYNTAX</span></span>

```
New-AzUserAssignedIdentity [-ResourceGroupName] <String> [-Name] <String> [-Location <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-Tag <Hashtable>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e809-105">說明</span><span class="sxs-lookup"><span data-stu-id="1e809-105">DESCRIPTION</span></span>
<span data-ttu-id="1e809-106">**新的-AzUserAssignedIdentity** Cmdlet 會建立新的使用者指派身分識別。</span><span class="sxs-lookup"><span data-stu-id="1e809-106">The **New-AzUserAssignedIdentity** cmdlet creates a new User Assigned Identity.</span></span> <span data-ttu-id="1e809-107">與已有的身分識別搭配使用時，會更新身分識別。</span><span class="sxs-lookup"><span data-stu-id="1e809-107">When used with an already existing identity, it updated the identity.</span></span>
<span data-ttu-id="1e809-108">若要將 Azure 資源管理器標記新增到身分識別，請使用 Set-AzResource Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1e809-108">To add Azure Resource Manager tags to the identity, please use the Set-AzResource cmdlet.</span></span>

## <span data-ttu-id="1e809-109">示例</span><span class="sxs-lookup"><span data-stu-id="1e809-109">EXAMPLES</span></span>

### <span data-ttu-id="1e809-110">範例1</span><span class="sxs-lookup"><span data-stu-id="1e809-110">Example 1</span></span>
<span data-ttu-id="1e809-111">這個範例 Cmdlet 會在 ResourceGroup 位置的 [資源群組 **PSRG** ] 底下，使用 [名稱 **ID1** ] 建立指派身分識別的新使用者。</span><span class="sxs-lookup"><span data-stu-id="1e809-111">This example cmdlet creates a new User Assigned Identity with name **ID1** under resource group **PSRG** in the location of the ResourceGroup.</span></span>

```powershell
PS C:\> New-AzUserAssignedIdentity -ResourceGroupName PSRG -Name ID1

Id                : /subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1

ResourceGroupName : PSRG

Name              : ID1

Location          : centralus

TenantId          : 493b860d-2741-480b-8b34-7b1d76e33c50

PrincipalId       : e34192f9-7831-4a02-bfe2-4c6d2fb4360d

ClientId          : a5e650a2-fdfe-4652-bb3b-109b64617cfd

ClientSecretUrl   : https://control-westus.identity.azure.net/subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG1/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1/credentials?tid=493b860d-2741-480b-8b34-7b1d76e33c50&oid=e34192f9-7831-4a02-bfe2-4c6d2fb4360d&aid=a5e650a2-fdfe-4652-bb3b-109b64617cfd

Type              : Microsoft.ManagedIdentity/userAssignedIdentities
```

### <span data-ttu-id="1e809-112">範例2</span><span class="sxs-lookup"><span data-stu-id="1e809-112">Example 2</span></span>
<span data-ttu-id="1e809-113">這個範例 Cmdlet 會在 westus 區域中的 [資源群組 **PSRG** ] 底下，使用 [名稱 **ID1** ] 建立指派身分識別的新使用者。</span><span class="sxs-lookup"><span data-stu-id="1e809-113">This example cmdlet creates a new User Assigned Identity with name **ID1** under the resource group **PSRG** in the westus region.</span></span>

```powershell
PS C:\> New-AzUserAssignedIdentity -ResourceGroupName PSRG -Name ID1 -Location westus

Id                : /subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1

ResourceGroupName : PSRG

Name              : ID1

Location          : westus

TenantId          : 493b860d-2741-480b-8b34-7b1d76e33c50

PrincipalId       : e34192f9-7831-4a02-bfe2-4c6d2fb4360d

ClientId          : a5e650a2-fdfe-4652-bb3b-109b64617cfd

ClientSecretUrl   : https://control-westus.identity.azure.net/subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1/credentials?tid=493b860d-2741-480b-8b34-7b1d76e33c50&oid=e34192f9-7831-4a02-bfe2-4c6d2fb4360d&aid=a5e650a2-fdfe-4652-bb3b-109b64617cfd

Type              : Microsoft.ManagedIdentity/userAssignedIdentities
```

## <span data-ttu-id="1e809-114">參數</span><span class="sxs-lookup"><span data-stu-id="1e809-114">PARAMETERS</span></span>

### <span data-ttu-id="1e809-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1e809-115">-AsJob</span></span>
<span data-ttu-id="1e809-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1e809-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1e809-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e809-117">-DefaultProfile</span></span>
<span data-ttu-id="1e809-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1e809-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e809-119">-位置</span><span class="sxs-lookup"><span data-stu-id="1e809-119">-Location</span></span>
<span data-ttu-id="1e809-120">應建立身分識別的 Azure 地區名稱。</span><span class="sxs-lookup"><span data-stu-id="1e809-120">The Azure region name where the Identity should be created.</span></span>

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

### <span data-ttu-id="1e809-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="1e809-121">-Name</span></span>
<span data-ttu-id="1e809-122">身分識別名稱。</span><span class="sxs-lookup"><span data-stu-id="1e809-122">The Identity name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e809-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e809-123">-ResourceGroupName</span></span>
<span data-ttu-id="1e809-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1e809-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e809-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="1e809-125">-Tag</span></span>
<span data-ttu-id="1e809-126">與身分識別相關聯的 Azure 資源管理器標記。</span><span class="sxs-lookup"><span data-stu-id="1e809-126">The Azure Resource Manager tags associated with the identity.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e809-127">-確認</span><span class="sxs-lookup"><span data-stu-id="1e809-127">-Confirm</span></span>
<span data-ttu-id="1e809-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1e809-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e809-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e809-129">-WhatIf</span></span>
<span data-ttu-id="1e809-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1e809-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e809-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1e809-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e809-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e809-132">CommonParameters</span></span>
<span data-ttu-id="1e809-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1e809-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e809-134">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1e809-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e809-135">輸入</span><span class="sxs-lookup"><span data-stu-id="1e809-135">INPUTS</span></span>

### <span data-ttu-id="1e809-136">System.object</span><span class="sxs-lookup"><span data-stu-id="1e809-136">System.String</span></span>

### <span data-ttu-id="1e809-137">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1e809-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1e809-138">輸出</span><span class="sxs-lookup"><span data-stu-id="1e809-138">OUTPUTS</span></span>

### <span data-ttu-id="1e809-139">PsUserAssignedIdentity 中的 ManagedServiceIdentity。</span><span class="sxs-lookup"><span data-stu-id="1e809-139">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span></span>

## <span data-ttu-id="1e809-140">筆記</span><span class="sxs-lookup"><span data-stu-id="1e809-140">NOTES</span></span>

## <span data-ttu-id="1e809-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="1e809-141">RELATED LINKS</span></span>