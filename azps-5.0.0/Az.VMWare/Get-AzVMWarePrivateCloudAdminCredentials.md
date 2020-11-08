---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwareprivatecloudadmincredentials
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWarePrivateCloudAdminCredentials.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWarePrivateCloudAdminCredentials.md
ms.openlocfilehash: 64552dada33249779e474dc72063f828c9336ffd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139884"
---
# <span data-ttu-id="a5606-101">Get-AzVMWarePrivateCloudAdminCredentials</span><span class="sxs-lookup"><span data-stu-id="a5606-101">Get-AzVMWarePrivateCloudAdminCredentials</span></span>

## <span data-ttu-id="a5606-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a5606-102">SYNOPSIS</span></span>
<span data-ttu-id="a5606-103">列出私人雲端的管理員認證</span><span class="sxs-lookup"><span data-stu-id="a5606-103">List the admin credentials for the private cloud</span></span>

## <span data-ttu-id="a5606-104">句法</span><span class="sxs-lookup"><span data-stu-id="a5606-104">SYNTAX</span></span>

```
Get-AzVMWarePrivateCloudAdminCredentials -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a5606-105">說明</span><span class="sxs-lookup"><span data-stu-id="a5606-105">DESCRIPTION</span></span>
<span data-ttu-id="a5606-106">列出私人雲端的管理員認證</span><span class="sxs-lookup"><span data-stu-id="a5606-106">List the admin credentials for the private cloud</span></span>

## <span data-ttu-id="a5606-107">示例</span><span class="sxs-lookup"><span data-stu-id="a5606-107">EXAMPLES</span></span>

### <span data-ttu-id="a5606-108">範例1：取得私有雲端的管理員認證</span><span class="sxs-lookup"><span data-stu-id="a5606-108">Example 1: Get admin credential of private cloud</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloudAdminCredentials -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

NsxtPassword NsxtUsername VcenterPassword VcenterUsername
------------ ------------ --------------- ---------------
************ admin        ************    cloudadmin@vsphere.local
```

<span data-ttu-id="a5606-109">取得私有雲端的管理員認證</span><span class="sxs-lookup"><span data-stu-id="a5606-109">Get admin credential of private cloud</span></span>

## <span data-ttu-id="a5606-110">參數</span><span class="sxs-lookup"><span data-stu-id="a5606-110">PARAMETERS</span></span>

### <span data-ttu-id="a5606-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5606-111">-DefaultProfile</span></span>
<span data-ttu-id="a5606-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a5606-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5606-113">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="a5606-113">-PrivateCloudName</span></span>
<span data-ttu-id="a5606-114">私有雲端的名稱</span><span class="sxs-lookup"><span data-stu-id="a5606-114">Name of the private cloud</span></span>

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

### <span data-ttu-id="a5606-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5606-115">-ResourceGroupName</span></span>
<span data-ttu-id="a5606-116">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a5606-116">The name of the resource group.</span></span>
<span data-ttu-id="a5606-117">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="a5606-117">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a5606-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a5606-118">-SubscriptionId</span></span>
<span data-ttu-id="a5606-119">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="a5606-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a5606-120">-確認</span><span class="sxs-lookup"><span data-stu-id="a5606-120">-Confirm</span></span>
<span data-ttu-id="a5606-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a5606-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5606-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5606-122">-WhatIf</span></span>
<span data-ttu-id="a5606-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a5606-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5606-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a5606-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5606-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5606-125">CommonParameters</span></span>
<span data-ttu-id="a5606-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a5606-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5606-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a5606-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5606-128">輸入</span><span class="sxs-lookup"><span data-stu-id="a5606-128">INPUTS</span></span>

## <span data-ttu-id="a5606-129">輸出</span><span class="sxs-lookup"><span data-stu-id="a5606-129">OUTPUTS</span></span>

### <span data-ttu-id="a5606-130">IAdminCredentials 中的 Api20200320 （）。</span><span class="sxs-lookup"><span data-stu-id="a5606-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IAdminCredentials</span></span>

## <span data-ttu-id="a5606-131">筆記</span><span class="sxs-lookup"><span data-stu-id="a5606-131">NOTES</span></span>

<span data-ttu-id="a5606-132">別名</span><span class="sxs-lookup"><span data-stu-id="a5606-132">ALIASES</span></span>

## <span data-ttu-id="a5606-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="a5606-133">RELATED LINKS</span></span>

