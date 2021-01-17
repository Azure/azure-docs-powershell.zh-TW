---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/connect-azconnectedmachine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Connect-AzConnectedMachine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Connect-AzConnectedMachine.md
ms.openlocfilehash: 281d456eb7612914bac546b3d361238bb5056626
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98446240"
---
# <span data-ttu-id="9f1eb-101">Connect-AzConnectedMachine</span><span class="sxs-lookup"><span data-stu-id="9f1eb-101">Connect-AzConnectedMachine</span></span>

## <span data-ttu-id="9f1eb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9f1eb-102">SYNOPSIS</span></span>
<span data-ttu-id="9f1eb-103">使用 API 登錄新電腦，進而在 ARM 中建立追蹤資源</span><span class="sxs-lookup"><span data-stu-id="9f1eb-103">API to register a new machine and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="9f1eb-104">句法</span><span class="sxs-lookup"><span data-stu-id="9f1eb-104">SYNTAX</span></span>

```
Connect-AzConnectedMachine [-ResourceGroupName] <String> [-Location] <String> [[-SubscriptionId] <String>]
 [[-Name] <String>] [[-DefaultProfile] <PSObject>] [[-PSSession] <PSSession[]>] [[-Tag] <Hashtable>]
 [[-Proxy] <Uri>] [<CommonParameters>]
```

## <span data-ttu-id="9f1eb-105">說明</span><span class="sxs-lookup"><span data-stu-id="9f1eb-105">DESCRIPTION</span></span>
<span data-ttu-id="9f1eb-106">使用 API 登錄新電腦，進而在 ARM 中建立追蹤資源</span><span class="sxs-lookup"><span data-stu-id="9f1eb-106">API to register a new machine and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="9f1eb-107">示例</span><span class="sxs-lookup"><span data-stu-id="9f1eb-107">EXAMPLES</span></span>

### <span data-ttu-id="9f1eb-108">範例1：將您目前所在的電腦 Onboards 為已連接的電腦</span><span class="sxs-lookup"><span data-stu-id="9f1eb-108">Example 1: Onboards the machine you're on as a connected machine</span></span>
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

<span data-ttu-id="9f1eb-109">Onboards 您正在使用的電腦做為已連接的電腦。</span><span class="sxs-lookup"><span data-stu-id="9f1eb-109">Onboards the machine you're on as a connected machine.</span></span>

### <span data-ttu-id="9f1eb-110">範例2：將遠端電腦 Onboards 為已連線的裝置</span><span class="sxs-lookup"><span data-stu-id="9f1eb-110">Example 2: Onboards a remote machine as a connected device</span></span>
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

<span data-ttu-id="9f1eb-111">使用 PowerShell remoting 將遠端電腦 Onboards 為已連線的裝置。</span><span class="sxs-lookup"><span data-stu-id="9f1eb-111">Onboards a remote machine as a connected device using PowerShell remoting.</span></span>
<span data-ttu-id="9f1eb-112">注意：目前只支援 Windows 作為目標。</span><span class="sxs-lookup"><span data-stu-id="9f1eb-112">Note: only Windows as the target is supported at this time.</span></span>

## <span data-ttu-id="9f1eb-113">參數</span><span class="sxs-lookup"><span data-stu-id="9f1eb-113">PARAMETERS</span></span>

### <span data-ttu-id="9f1eb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f1eb-114">-DefaultProfile</span></span>
<span data-ttu-id="9f1eb-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9f1eb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f1eb-116">-位置</span><span class="sxs-lookup"><span data-stu-id="9f1eb-116">-Location</span></span>
<span data-ttu-id="9f1eb-117">建立的 ConnectedMachine 的位置。</span><span class="sxs-lookup"><span data-stu-id="9f1eb-117">The location for the created ConnectedMachine.</span></span>

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

### <span data-ttu-id="9f1eb-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="9f1eb-118">-Name</span></span>
<span data-ttu-id="9f1eb-119">此電腦將使用的名稱。</span><span class="sxs-lookup"><span data-stu-id="9f1eb-119">The name that will be used for this machine.</span></span>
<span data-ttu-id="9f1eb-120">預設會使用主機名稱。</span><span class="sxs-lookup"><span data-stu-id="9f1eb-120">The hostname is used by default.</span></span>

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

### <span data-ttu-id="9f1eb-121">-Proxy</span><span class="sxs-lookup"><span data-stu-id="9f1eb-121">-Proxy</span></span>
<span data-ttu-id="9f1eb-122">要使用之 proxy 伺服器的 URI</span><span class="sxs-lookup"><span data-stu-id="9f1eb-122">The URI for the proxy server to use</span></span>

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

### <span data-ttu-id="9f1eb-123">-PSSession</span><span class="sxs-lookup"><span data-stu-id="9f1eb-123">-PSSession</span></span>
<span data-ttu-id="9f1eb-124">在指定時，會在每個 PSSession 內執行 onboards 電腦至 Azure 的命令。</span><span class="sxs-lookup"><span data-stu-id="9f1eb-124">When specified, the command that onboards machines to Azure will be run within each PSSession.</span></span>
<span data-ttu-id="9f1eb-125">注意：這只適用于 Windows。</span><span class="sxs-lookup"><span data-stu-id="9f1eb-125">NOTE: This only works on Windows for now.</span></span>

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

### <span data-ttu-id="9f1eb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f1eb-126">-ResourceGroupName</span></span>
<span data-ttu-id="9f1eb-127">您想要新增電腦的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9f1eb-127">The name of the resource group you want to add the machine to.</span></span>

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

### <span data-ttu-id="9f1eb-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9f1eb-128">-SubscriptionId</span></span>
<span data-ttu-id="9f1eb-129">您想要新增電腦的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="9f1eb-129">The ID of the subscription you want to add the machine to.</span></span>

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

### <span data-ttu-id="9f1eb-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="9f1eb-130">-Tag</span></span>
<span data-ttu-id="9f1eb-131">資源標記。</span><span class="sxs-lookup"><span data-stu-id="9f1eb-131">Resource tags.</span></span>

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

### <span data-ttu-id="9f1eb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f1eb-132">CommonParameters</span></span>
<span data-ttu-id="9f1eb-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9f1eb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f1eb-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9f1eb-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f1eb-135">輸入</span><span class="sxs-lookup"><span data-stu-id="9f1eb-135">INPUTS</span></span>

## <span data-ttu-id="9f1eb-136">輸出</span><span class="sxs-lookup"><span data-stu-id="9f1eb-136">OUTPUTS</span></span>

## <span data-ttu-id="9f1eb-137">筆記</span><span class="sxs-lookup"><span data-stu-id="9f1eb-137">NOTES</span></span>

<span data-ttu-id="9f1eb-138">別名</span><span class="sxs-lookup"><span data-stu-id="9f1eb-138">ALIASES</span></span>

## <span data-ttu-id="9f1eb-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="9f1eb-139">RELATED LINKS</span></span>

