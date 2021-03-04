---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/get-azcloudserviceroleinstanceremotedesktopfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstanceRemoteDesktopFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstanceRemoteDesktopFile.md
ms.openlocfilehash: 74948fe91e4a2823c9bbe8e8c0e50ade33612e18
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912109"
---
# <span data-ttu-id="77682-101">Get-AzCloudServiceRoleInstanceRemoteDesktopFile</span><span class="sxs-lookup"><span data-stu-id="77682-101">Get-AzCloudServiceRoleInstanceRemoteDesktopFile</span></span>

## <span data-ttu-id="77682-102">簡介</span><span class="sxs-lookup"><span data-stu-id="77682-102">SYNOPSIS</span></span>
<span data-ttu-id="77682-103">在雲端服務中為角色實例獲得遠端桌面檔案。</span><span class="sxs-lookup"><span data-stu-id="77682-103">Gets a remote desktop file for a role instance in a cloud service.</span></span>

## <span data-ttu-id="77682-104">語法</span><span class="sxs-lookup"><span data-stu-id="77682-104">SYNTAX</span></span>

```
Get-AzCloudServiceRoleInstanceRemoteDesktopFile -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstanceName <String> -OutFile <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [-PassThru] [<CommonParameters>]
```

## <span data-ttu-id="77682-105">描述</span><span class="sxs-lookup"><span data-stu-id="77682-105">DESCRIPTION</span></span>
<span data-ttu-id="77682-106">在雲端服務中為角色實例獲得遠端桌面檔案。</span><span class="sxs-lookup"><span data-stu-id="77682-106">Gets a remote desktop file for a role instance in a cloud service.</span></span>

## <span data-ttu-id="77682-107">例子</span><span class="sxs-lookup"><span data-stu-id="77682-107">EXAMPLES</span></span>

### <span data-ttu-id="77682-108">範例 1：取得 RDP 檔案</span><span class="sxs-lookup"><span data-stu-id="77682-108">Example 1: Get an RDP file</span></span>
```powershell
PS C:\> Get-AzCloudServiceRoleInstanceRemoteDesktopFile -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstanceName "ContosoFrontEnd_IN_0" -OutFile "C:\temp\ContosoFrontEnd_IN_0.rdp"
```

<span data-ttu-id="77682-109">此命令會針對名稱為 ContosoFrontEnd IN 0 之雲端服務的名稱為 ContosoCS 的角色實例獲得 RDP 檔案，該角色實例屬於 \_ \_ 名為 ContosOrg 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="77682-109">This command gets an RDP file for the role instance named ContosoFrontEnd\_IN\_0 of cloud Service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="77682-110">參數</span><span class="sxs-lookup"><span data-stu-id="77682-110">PARAMETERS</span></span>

### <span data-ttu-id="77682-111">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="77682-111">-CloudServiceName</span></span>
<span data-ttu-id="77682-112">.</span><span class="sxs-lookup"><span data-stu-id="77682-112">.</span></span>

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

### <span data-ttu-id="77682-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77682-113">-DefaultProfile</span></span>
<span data-ttu-id="77682-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="77682-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77682-115">-OutFile</span><span class="sxs-lookup"><span data-stu-id="77682-115">-OutFile</span></span>
<span data-ttu-id="77682-116">寫入輸出檔案的路徑</span><span class="sxs-lookup"><span data-stu-id="77682-116">Path to write output file to</span></span>

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

### <span data-ttu-id="77682-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="77682-117">-PassThru</span></span>
<span data-ttu-id="77682-118">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="77682-118">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="77682-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77682-119">-ResourceGroupName</span></span>
<span data-ttu-id="77682-120">.</span><span class="sxs-lookup"><span data-stu-id="77682-120">.</span></span>

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

### <span data-ttu-id="77682-121">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="77682-121">-RoleInstanceName</span></span>
<span data-ttu-id="77682-122">角色實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="77682-122">Name of the role instance.</span></span>

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

### <span data-ttu-id="77682-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="77682-123">-SubscriptionId</span></span>
<span data-ttu-id="77682-124">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="77682-124">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="77682-125">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="77682-125">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="77682-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77682-126">CommonParameters</span></span>
<span data-ttu-id="77682-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="77682-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77682-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="77682-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77682-129">輸入</span><span class="sxs-lookup"><span data-stu-id="77682-129">INPUTS</span></span>

## <span data-ttu-id="77682-130">輸出</span><span class="sxs-lookup"><span data-stu-id="77682-130">OUTPUTS</span></span>

### <span data-ttu-id="77682-131">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="77682-131">System.Boolean</span></span>

## <span data-ttu-id="77682-132">筆記</span><span class="sxs-lookup"><span data-stu-id="77682-132">NOTES</span></span>

<span data-ttu-id="77682-133">別名</span><span class="sxs-lookup"><span data-stu-id="77682-133">ALIASES</span></span>

## <span data-ttu-id="77682-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="77682-134">RELATED LINKS</span></span>

