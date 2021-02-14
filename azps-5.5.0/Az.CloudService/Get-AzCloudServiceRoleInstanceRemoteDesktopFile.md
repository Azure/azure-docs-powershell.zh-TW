---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/get-azcloudserviceroleinstanceremotedesktopfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstanceRemoteDesktopFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstanceRemoteDesktopFile.md
ms.openlocfilehash: 2b4133942a3aa7c4e9339579465942ade96c5709
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100129914"
---
# <span data-ttu-id="f144b-101">Get-AzCloudServiceRoleInstanceRemoteDesktopFile</span><span class="sxs-lookup"><span data-stu-id="f144b-101">Get-AzCloudServiceRoleInstanceRemoteDesktopFile</span></span>

## <span data-ttu-id="f144b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f144b-102">SYNOPSIS</span></span>
<span data-ttu-id="f144b-103">取得雲端服務中角色實例的遠端桌面檔案。</span><span class="sxs-lookup"><span data-stu-id="f144b-103">Gets a remote desktop file for a role instance in a cloud service.</span></span>

## <span data-ttu-id="f144b-104">句法</span><span class="sxs-lookup"><span data-stu-id="f144b-104">SYNTAX</span></span>

```
Get-AzCloudServiceRoleInstanceRemoteDesktopFile -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstanceName <String> -OutFile <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [-PassThru] [<CommonParameters>]
```

## <span data-ttu-id="f144b-105">說明</span><span class="sxs-lookup"><span data-stu-id="f144b-105">DESCRIPTION</span></span>
<span data-ttu-id="f144b-106">取得雲端服務中角色實例的遠端桌面檔案。</span><span class="sxs-lookup"><span data-stu-id="f144b-106">Gets a remote desktop file for a role instance in a cloud service.</span></span>

## <span data-ttu-id="f144b-107">示例</span><span class="sxs-lookup"><span data-stu-id="f144b-107">EXAMPLES</span></span>

### <span data-ttu-id="f144b-108">範例1：取得 RDP 檔案</span><span class="sxs-lookup"><span data-stu-id="f144b-108">Example 1: Get an RDP file</span></span>
```powershell
PS C:\> Get-AzCloudServiceRoleInstanceRemoteDesktopFile -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstanceName "ContosoFrontEnd_IN_0" -OutFile "C:\temp\ContosoFrontEnd_IN_0.rdp"
```

<span data-ttu-id="f144b-109">這個命令會取得名為 ContosoFrontEnd 之角色實例的 RDP 檔案，該檔案屬於名為 \_ \_ ContosoCS 的雲端服務，而該名稱屬於名為 ContosOrg 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="f144b-109">This command gets an RDP file for the role instance named ContosoFrontEnd\_IN\_0 of cloud Service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="f144b-110">參數</span><span class="sxs-lookup"><span data-stu-id="f144b-110">PARAMETERS</span></span>

### <span data-ttu-id="f144b-111">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="f144b-111">-CloudServiceName</span></span>
<span data-ttu-id="f144b-112">.</span><span class="sxs-lookup"><span data-stu-id="f144b-112">.</span></span>

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

### <span data-ttu-id="f144b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f144b-113">-DefaultProfile</span></span>
<span data-ttu-id="f144b-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f144b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f144b-115">-OutFile</span><span class="sxs-lookup"><span data-stu-id="f144b-115">-OutFile</span></span>
<span data-ttu-id="f144b-116">要寫入輸出檔案的路徑</span><span class="sxs-lookup"><span data-stu-id="f144b-116">Path to write output file to</span></span>

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

### <span data-ttu-id="f144b-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f144b-117">-PassThru</span></span>
<span data-ttu-id="f144b-118">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="f144b-118">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f144b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f144b-119">-ResourceGroupName</span></span>
<span data-ttu-id="f144b-120">.</span><span class="sxs-lookup"><span data-stu-id="f144b-120">.</span></span>

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

### <span data-ttu-id="f144b-121">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="f144b-121">-RoleInstanceName</span></span>
<span data-ttu-id="f144b-122">角色實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="f144b-122">Name of the role instance.</span></span>

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

### <span data-ttu-id="f144b-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f144b-123">-SubscriptionId</span></span>
<span data-ttu-id="f144b-124">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="f144b-124">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f144b-125">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="f144b-125">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f144b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f144b-126">CommonParameters</span></span>
<span data-ttu-id="f144b-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f144b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f144b-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f144b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f144b-129">輸入</span><span class="sxs-lookup"><span data-stu-id="f144b-129">INPUTS</span></span>

## <span data-ttu-id="f144b-130">輸出</span><span class="sxs-lookup"><span data-stu-id="f144b-130">OUTPUTS</span></span>

### <span data-ttu-id="f144b-131">System.object</span><span class="sxs-lookup"><span data-stu-id="f144b-131">System.Boolean</span></span>

## <span data-ttu-id="f144b-132">筆記</span><span class="sxs-lookup"><span data-stu-id="f144b-132">NOTES</span></span>

<span data-ttu-id="f144b-133">別名</span><span class="sxs-lookup"><span data-stu-id="f144b-133">ALIASES</span></span>

## <span data-ttu-id="f144b-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="f144b-134">RELATED LINKS</span></span>

