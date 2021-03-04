---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/powershell/module/az.connectedmachine/connect-azconnectedmachine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Connect-AzConnectedMachine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Connect-AzConnectedMachine.md
ms.openlocfilehash: b0e52f6d163579e1d481f841d3a58e8b15c6658b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917029"
---
# <span data-ttu-id="f41d4-101">Connect-AzConnectedMachine</span><span class="sxs-lookup"><span data-stu-id="f41d4-101">Connect-AzConnectedMachine</span></span>

## <span data-ttu-id="f41d4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f41d4-102">SYNOPSIS</span></span>
<span data-ttu-id="f41d4-103">API 以註冊新電腦，進而在 ARM 中建立追蹤資源</span><span class="sxs-lookup"><span data-stu-id="f41d4-103">API to register a new machine and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="f41d4-104">語法</span><span class="sxs-lookup"><span data-stu-id="f41d4-104">SYNTAX</span></span>

```
Connect-AzConnectedMachine [-ResourceGroupName] <String> [-Location] <String> [[-SubscriptionId] <String>]
 [[-Name] <String>] [[-DefaultProfile] <PSObject>] [[-PSSession] <PSSession[]>] [[-Tag] <Hashtable>]
 [[-Proxy] <Uri>] [<CommonParameters>]
```

## <span data-ttu-id="f41d4-105">描述</span><span class="sxs-lookup"><span data-stu-id="f41d4-105">DESCRIPTION</span></span>
<span data-ttu-id="f41d4-106">API 以註冊新電腦，進而在 ARM 中建立追蹤資源</span><span class="sxs-lookup"><span data-stu-id="f41d4-106">API to register a new machine and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="f41d4-107">例子</span><span class="sxs-lookup"><span data-stu-id="f41d4-107">EXAMPLES</span></span>

### <span data-ttu-id="f41d4-108">範例 1：以連接電腦方式將您安裝的機器上線</span><span class="sxs-lookup"><span data-stu-id="f41d4-108">Example 1: Onboards the machine you're on as a connected machine</span></span>
```powershell
PS C:\> Connect-AzConnectedMachine -ResourceGroupName contoso-connected-machines -Name linux_eastus1_1 -Location eastus

< truncated output of installing the azcmagent >

time="2020-08-07T13:13:25-07:00" level=info msg="Onboarding Machine. It usually takes a few minutes to complete. Sometimes it may take longer depending on network and server load status."
time="2020-08-07T13:13:25-07:00" level=info msg="Check network connectivity to all endpoints..."
time="2020-08-07T13:13:29-07:00" level=info msg="All endpoints are available... continue onboarding"
time="2020-08-07T13:13:50-07:00" level=info msg="Successfully Onboarded Resource to Azure" VM Id=978ab182-6cf0-4de3-a58b-53c8d0a3235e

Name             Location OSName   Status     ProvisioningState
----             -------- ------   ------     -----------------
linux_eastus1_1  eastus   linux    Connected  Succeeded
```

<span data-ttu-id="f41d4-109">以連接電腦方式將您上線的機器上線。</span><span class="sxs-lookup"><span data-stu-id="f41d4-109">Onboards the machine you're on as a connected machine.</span></span>

### <span data-ttu-id="f41d4-110">範例 2：將遠端電腦當做連接裝置上線</span><span class="sxs-lookup"><span data-stu-id="f41d4-110">Example 2: Onboards a remote machine as a connected device</span></span>
```powershell
PS C:\> $session = Connect-PSSession -ComputerName WINBOX
PS C:\> Connect-AzConnectedMachine -ResourceGroupName contoso-rg -Name win_eastus1_1 -Location eastus -PSSession $session

< truncated output of installing the azcmagent >

time="2020-08-07T13:13:25-07:00" level=info msg="Onboarding Machine. It usually takes a few minutes to complete. Sometimes it may take longer depending on network and server load status."
time="2020-08-07T13:13:25-07:00" level=info msg="Check network connectivity to all endpoints..."
time="2020-08-07T13:13:29-07:00" level=info msg="All endpoints are available... continue onboarding"
time="2020-08-07T13:13:50-07:00" level=info msg="Successfully Onboarded Resource to Azure" VM Id=978ab182-6cf0-4de3-a58b-53c8d0a3236a

Name           Location OSName   Status     ProvisioningState
----           -------- ------   ------     -----------------
win_eastus1_1  eastus   windows  Connected  Succeeded
```

<span data-ttu-id="f41d4-111">使用 PowerShell 重做連接裝置，將遠端電腦上線。</span><span class="sxs-lookup"><span data-stu-id="f41d4-111">Onboards a remote machine as a connected device using PowerShell remoting.</span></span>
<span data-ttu-id="f41d4-112">注意：目前僅支援 Windows 做為目標。</span><span class="sxs-lookup"><span data-stu-id="f41d4-112">Note: only Windows as the target is supported at this time.</span></span>

## <span data-ttu-id="f41d4-113">參數</span><span class="sxs-lookup"><span data-stu-id="f41d4-113">PARAMETERS</span></span>

### <span data-ttu-id="f41d4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f41d4-114">-DefaultProfile</span></span>
<span data-ttu-id="f41d4-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f41d4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f41d4-116">-位置</span><span class="sxs-lookup"><span data-stu-id="f41d4-116">-Location</span></span>
<span data-ttu-id="f41d4-117">已建立之 ConnectedMachine 的位置。</span><span class="sxs-lookup"><span data-stu-id="f41d4-117">The location for the created ConnectedMachine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f41d4-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="f41d4-118">-Name</span></span>
<span data-ttu-id="f41d4-119">此電腦將會使用的名稱。</span><span class="sxs-lookup"><span data-stu-id="f41d4-119">The name that will be used for this machine.</span></span>
<span data-ttu-id="f41d4-120">主機名稱預設為使用。</span><span class="sxs-lookup"><span data-stu-id="f41d4-120">The hostname is used by default.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f41d4-121">-Proxy</span><span class="sxs-lookup"><span data-stu-id="f41d4-121">-Proxy</span></span>
<span data-ttu-id="f41d4-122">Proxy 伺服器使用的 URI</span><span class="sxs-lookup"><span data-stu-id="f41d4-122">The URI for the proxy server to use</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f41d4-123">-PSSession</span><span class="sxs-lookup"><span data-stu-id="f41d4-123">-PSSession</span></span>
<span data-ttu-id="f41d4-124">指定時，將電腦上標至 Azure 的命令將會在每個 PSSession 中執行。</span><span class="sxs-lookup"><span data-stu-id="f41d4-124">When specified, the command that onboards machines to Azure will be run within each PSSession.</span></span>
<span data-ttu-id="f41d4-125">注意：這僅適用于 Windows 目前。</span><span class="sxs-lookup"><span data-stu-id="f41d4-125">NOTE: This only works on Windows for now.</span></span>

```yaml
Type: System.Management.Automation.Runspaces.PSSession[]
Parameter Sets: (All)
Aliases: Session

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f41d4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f41d4-126">-ResourceGroupName</span></span>
<span data-ttu-id="f41d4-127">您想要新增電腦的資源組名。</span><span class="sxs-lookup"><span data-stu-id="f41d4-127">The name of the resource group you want to add the machine to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f41d4-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f41d4-128">-SubscriptionId</span></span>
<span data-ttu-id="f41d4-129">這是要新增電腦之訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f41d4-129">The ID of the subscription you want to add the machine to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f41d4-130">-標記</span><span class="sxs-lookup"><span data-stu-id="f41d4-130">-Tag</span></span>
<span data-ttu-id="f41d4-131">資源標記。</span><span class="sxs-lookup"><span data-stu-id="f41d4-131">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f41d4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f41d4-132">CommonParameters</span></span>
<span data-ttu-id="f41d4-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f41d4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f41d4-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f41d4-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f41d4-135">輸入</span><span class="sxs-lookup"><span data-stu-id="f41d4-135">INPUTS</span></span>

## <span data-ttu-id="f41d4-136">輸出</span><span class="sxs-lookup"><span data-stu-id="f41d4-136">OUTPUTS</span></span>

## <span data-ttu-id="f41d4-137">筆記</span><span class="sxs-lookup"><span data-stu-id="f41d4-137">NOTES</span></span>

<span data-ttu-id="f41d4-138">別名</span><span class="sxs-lookup"><span data-stu-id="f41d4-138">ALIASES</span></span>

## <span data-ttu-id="f41d4-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="f41d4-139">RELATED LINKS</span></span>

