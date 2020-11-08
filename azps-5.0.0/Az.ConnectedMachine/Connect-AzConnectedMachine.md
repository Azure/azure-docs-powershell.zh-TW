---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/connect-azconnectedmachine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Connect-AzConnectedMachine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Connect-AzConnectedMachine.md
ms.openlocfilehash: 281d456eb7612914bac546b3d361238bb5056626
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138195"
---
# <span data-ttu-id="91396-101">Connect-AzConnectedMachine</span><span class="sxs-lookup"><span data-stu-id="91396-101">Connect-AzConnectedMachine</span></span>

## <span data-ttu-id="91396-102">摘要</span><span class="sxs-lookup"><span data-stu-id="91396-102">SYNOPSIS</span></span>
<span data-ttu-id="91396-103">使用 API 登錄新電腦，進而在 ARM 中建立追蹤資源</span><span class="sxs-lookup"><span data-stu-id="91396-103">API to register a new machine and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="91396-104">句法</span><span class="sxs-lookup"><span data-stu-id="91396-104">SYNTAX</span></span>

```
Connect-AzConnectedMachine [-ResourceGroupName] <String> [-Location] <String> [[-SubscriptionId] <String>]
 [[-Name] <String>] [[-DefaultProfile] <PSObject>] [[-PSSession] <PSSession[]>] [[-Tag] <Hashtable>]
 [[-Proxy] <Uri>] [<CommonParameters>]
```

## <span data-ttu-id="91396-105">說明</span><span class="sxs-lookup"><span data-stu-id="91396-105">DESCRIPTION</span></span>
<span data-ttu-id="91396-106">使用 API 登錄新電腦，進而在 ARM 中建立追蹤資源</span><span class="sxs-lookup"><span data-stu-id="91396-106">API to register a new machine and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="91396-107">示例</span><span class="sxs-lookup"><span data-stu-id="91396-107">EXAMPLES</span></span>

### <span data-ttu-id="91396-108">範例1：將您目前所在的電腦 Onboards 為已連接的電腦</span><span class="sxs-lookup"><span data-stu-id="91396-108">Example 1: Onboards the machine you're on as a connected machine</span></span>
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

<span data-ttu-id="91396-109">Onboards 您正在使用的電腦做為已連接的電腦。</span><span class="sxs-lookup"><span data-stu-id="91396-109">Onboards the machine you're on as a connected machine.</span></span>

### <span data-ttu-id="91396-110">範例2：將遠端電腦 Onboards 為已連線的裝置</span><span class="sxs-lookup"><span data-stu-id="91396-110">Example 2: Onboards a remote machine as a connected device</span></span>
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

<span data-ttu-id="91396-111">使用 PowerShell remoting 將遠端電腦 Onboards 為已連線的裝置。</span><span class="sxs-lookup"><span data-stu-id="91396-111">Onboards a remote machine as a connected device using PowerShell remoting.</span></span>
<span data-ttu-id="91396-112">注意：目前只支援 Windows 作為目標。</span><span class="sxs-lookup"><span data-stu-id="91396-112">Note: only Windows as the target is supported at this time.</span></span>

## <span data-ttu-id="91396-113">參數</span><span class="sxs-lookup"><span data-stu-id="91396-113">PARAMETERS</span></span>

### <span data-ttu-id="91396-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91396-114">-DefaultProfile</span></span>
<span data-ttu-id="91396-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="91396-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91396-116">-位置</span><span class="sxs-lookup"><span data-stu-id="91396-116">-Location</span></span>
<span data-ttu-id="91396-117">建立的 ConnectedMachine 的位置。</span><span class="sxs-lookup"><span data-stu-id="91396-117">The location for the created ConnectedMachine.</span></span>

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

### <span data-ttu-id="91396-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="91396-118">-Name</span></span>
<span data-ttu-id="91396-119">此電腦將使用的名稱。</span><span class="sxs-lookup"><span data-stu-id="91396-119">The name that will be used for this machine.</span></span>
<span data-ttu-id="91396-120">預設會使用主機名稱。</span><span class="sxs-lookup"><span data-stu-id="91396-120">The hostname is used by default.</span></span>

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

### <span data-ttu-id="91396-121">-Proxy</span><span class="sxs-lookup"><span data-stu-id="91396-121">-Proxy</span></span>
<span data-ttu-id="91396-122">要使用之 proxy 伺服器的 URI</span><span class="sxs-lookup"><span data-stu-id="91396-122">The URI for the proxy server to use</span></span>

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

### <span data-ttu-id="91396-123">-PSSession</span><span class="sxs-lookup"><span data-stu-id="91396-123">-PSSession</span></span>
<span data-ttu-id="91396-124">在指定時，會在每個 PSSession 內執行 onboards 電腦至 Azure 的命令。</span><span class="sxs-lookup"><span data-stu-id="91396-124">When specified, the command that onboards machines to Azure will be run within each PSSession.</span></span>
<span data-ttu-id="91396-125">注意：這只適用于 Windows。</span><span class="sxs-lookup"><span data-stu-id="91396-125">NOTE: This only works on Windows for now.</span></span>

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

### <span data-ttu-id="91396-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91396-126">-ResourceGroupName</span></span>
<span data-ttu-id="91396-127">您想要新增電腦的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="91396-127">The name of the resource group you want to add the machine to.</span></span>

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

### <span data-ttu-id="91396-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="91396-128">-SubscriptionId</span></span>
<span data-ttu-id="91396-129">您想要新增電腦的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="91396-129">The ID of the subscription you want to add the machine to.</span></span>

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

### <span data-ttu-id="91396-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="91396-130">-Tag</span></span>
<span data-ttu-id="91396-131">資源標記。</span><span class="sxs-lookup"><span data-stu-id="91396-131">Resource tags.</span></span>

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

### <span data-ttu-id="91396-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91396-132">CommonParameters</span></span>
<span data-ttu-id="91396-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="91396-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91396-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="91396-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91396-135">輸入</span><span class="sxs-lookup"><span data-stu-id="91396-135">INPUTS</span></span>

## <span data-ttu-id="91396-136">輸出</span><span class="sxs-lookup"><span data-stu-id="91396-136">OUTPUTS</span></span>

## <span data-ttu-id="91396-137">筆記</span><span class="sxs-lookup"><span data-stu-id="91396-137">NOTES</span></span>

<span data-ttu-id="91396-138">別名</span><span class="sxs-lookup"><span data-stu-id="91396-138">ALIASES</span></span>

## <span data-ttu-id="91396-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="91396-139">RELATED LINKS</span></span>

