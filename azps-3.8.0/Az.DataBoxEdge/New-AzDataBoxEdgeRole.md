---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeRole.md
ms.openlocfilehash: aa44399adcfd5e39d956215b7ca824e5ef9abd60
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959339"
---
# <span data-ttu-id="38d38-101">New-AzDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="38d38-101">New-AzDataBoxEdgeRole</span></span>

## <span data-ttu-id="38d38-102">摘要</span><span class="sxs-lookup"><span data-stu-id="38d38-102">SYNOPSIS</span></span>
<span data-ttu-id="38d38-103">為裝置建立新的角色</span><span class="sxs-lookup"><span data-stu-id="38d38-103">Creates a new Role for a device</span></span>

## <span data-ttu-id="38d38-104">句法</span><span class="sxs-lookup"><span data-stu-id="38d38-104">SYNTAX</span></span>

### <span data-ttu-id="38d38-105">ConnectionStringParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="38d38-105">ConnectionStringParameterSet (Default)</span></span>
```
New-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-ConnectionString]
 -IotDeviceConnectionString <SecureString> -IotEdgeDeviceConnectionString <SecureString>
 -EncryptionKey <SecureString> -Platform <String> -RoleStatus <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38d38-106">IotParameterSet</span><span class="sxs-lookup"><span data-stu-id="38d38-106">IotParameterSet</span></span>
```
New-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-DeviceProperty]
 -IotDeviceId <String> -IotDeviceAccessKey <SecureString> -IotEdgeDeviceId <String>
 -IotEdgeDeviceAccessKey <SecureString> -IotHostHub <String> -EncryptionKey <SecureString> -Platform <String>
 -RoleStatus <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="38d38-107">說明</span><span class="sxs-lookup"><span data-stu-id="38d38-107">DESCRIPTION</span></span>
<span data-ttu-id="38d38-108">**新的-AzDataBoxEdgeRole** Cmdlet 會為數據盒 Edge 裝置建立新的角色。</span><span class="sxs-lookup"><span data-stu-id="38d38-108">The **New-AzDataBoxEdgeRole** cmdlet creates a new Role for a Data Box Edge device.</span></span>

## <span data-ttu-id="38d38-109">示例</span><span class="sxs-lookup"><span data-stu-id="38d38-109">EXAMPLES</span></span>

### <span data-ttu-id="38d38-110">範例1</span><span class="sxs-lookup"><span data-stu-id="38d38-110">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name iotrole -DeviceProperties
 -IotDeviceId iotDeviceId -IotDeviceAccessKey iotAccessKey -IotEdgeDeviceId iotEdgeDeviceId -IotEdgeDeviceAccessKey iotEdgeDeviceAccessKey
 -IotHostHub "ehub.azure-devices.net" -EncryptionKey @SecureString -Platform Linux -RoleStatus Enabled

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceId   iotDeviceId  resourceGroupName
```

## <span data-ttu-id="38d38-111">參數</span><span class="sxs-lookup"><span data-stu-id="38d38-111">PARAMETERS</span></span>

### <span data-ttu-id="38d38-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="38d38-112">-AsJob</span></span>
<span data-ttu-id="38d38-113">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="38d38-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="38d38-114">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="38d38-114">-ConnectionString</span></span>
<span data-ttu-id="38d38-115">提供連接字串</span><span class="sxs-lookup"><span data-stu-id="38d38-115">To Provide Connection Strings</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ConnectionStringParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38d38-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38d38-116">-DefaultProfile</span></span>
<span data-ttu-id="38d38-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="38d38-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38d38-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="38d38-118">-DeviceName</span></span>
<span data-ttu-id="38d38-119">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="38d38-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38d38-120">-DeviceProperty</span><span class="sxs-lookup"><span data-stu-id="38d38-120">-DeviceProperty</span></span>
<span data-ttu-id="38d38-121">提供裝置屬性</span><span class="sxs-lookup"><span data-stu-id="38d38-121">To Provide Device Properties</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: IotParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38d38-122">-Encryption.encryptionkey</span><span class="sxs-lookup"><span data-stu-id="38d38-122">-EncryptionKey</span></span>
<span data-ttu-id="38d38-123">Edge 裝置的加密金鑰</span><span class="sxs-lookup"><span data-stu-id="38d38-123">Encryption key of the Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38d38-124">-IotDeviceAccessKey</span><span class="sxs-lookup"><span data-stu-id="38d38-124">-IotDeviceAccessKey</span></span>
<span data-ttu-id="38d38-125">Iot 裝置便捷鍵</span><span class="sxs-lookup"><span data-stu-id="38d38-125">Iot Device Access Key</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: IotParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38d38-126">-IotDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="38d38-126">-IotDeviceConnectionString</span></span>
<span data-ttu-id="38d38-127">請提供 IOT 裝置的連線字串</span><span class="sxs-lookup"><span data-stu-id="38d38-127">Please provide connection string of IOT Device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ConnectionStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38d38-128">-IotDeviceId</span><span class="sxs-lookup"><span data-stu-id="38d38-128">-IotDeviceId</span></span>
<span data-ttu-id="38d38-129">Iot 裝置的裝置識別碼</span><span class="sxs-lookup"><span data-stu-id="38d38-129">Device Id of the Iot Device</span></span>

```yaml
Type: System.String
Parameter Sets: IotParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38d38-130">-IotEdgeDeviceAccessKey</span><span class="sxs-lookup"><span data-stu-id="38d38-130">-IotEdgeDeviceAccessKey</span></span>
<span data-ttu-id="38d38-131">Iot Edge 裝置的便捷鍵</span><span class="sxs-lookup"><span data-stu-id="38d38-131">Access key of the Iot Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: IotParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38d38-132">-IotEdgeDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="38d38-132">-IotEdgeDeviceConnectionString</span></span>
<span data-ttu-id="38d38-133">請提供 Edge 裝置的連線字串</span><span class="sxs-lookup"><span data-stu-id="38d38-133">Please provide connection string of Edge Device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ConnectionStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38d38-134">-IotEdgeDeviceId</span><span class="sxs-lookup"><span data-stu-id="38d38-134">-IotEdgeDeviceId</span></span>
<span data-ttu-id="38d38-135">Iot Edge 裝置的識別碼</span><span class="sxs-lookup"><span data-stu-id="38d38-135">Id of the Iot Edge Device</span></span>

```yaml
Type: System.String
Parameter Sets: IotParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38d38-136">-IotHostHub</span><span class="sxs-lookup"><span data-stu-id="38d38-136">-IotHostHub</span></span>
<span data-ttu-id="38d38-137">Hosthub 位址</span><span class="sxs-lookup"><span data-stu-id="38d38-137">Hosthub address</span></span>

```yaml
Type: System.String
Parameter Sets: IotParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38d38-138">-名稱</span><span class="sxs-lookup"><span data-stu-id="38d38-138">-Name</span></span>
<span data-ttu-id="38d38-139">資源名稱</span><span class="sxs-lookup"><span data-stu-id="38d38-139">Resource Name</span></span>

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

### <span data-ttu-id="38d38-140">-平臺</span><span class="sxs-lookup"><span data-stu-id="38d38-140">-Platform</span></span>
<span data-ttu-id="38d38-141">提供適用于 ex： Linux 的平臺</span><span class="sxs-lookup"><span data-stu-id="38d38-141">Provide the Platform, for ex: Linux</span></span>

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

### <span data-ttu-id="38d38-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38d38-142">-ResourceGroupName</span></span>
<span data-ttu-id="38d38-143">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="38d38-143">Resource Group Name</span></span>

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

### <span data-ttu-id="38d38-144">-RoleStatus</span><span class="sxs-lookup"><span data-stu-id="38d38-144">-RoleStatus</span></span>
<span data-ttu-id="38d38-145">提供狀態 [啟用]/[停用]</span><span class="sxs-lookup"><span data-stu-id="38d38-145">Provide the status enable/disable</span></span>

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

### <span data-ttu-id="38d38-146">-確認</span><span class="sxs-lookup"><span data-stu-id="38d38-146">-Confirm</span></span>
<span data-ttu-id="38d38-147">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="38d38-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38d38-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38d38-148">-WhatIf</span></span>
<span data-ttu-id="38d38-149">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="38d38-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="38d38-150">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="38d38-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38d38-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38d38-151">CommonParameters</span></span>
<span data-ttu-id="38d38-152">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="38d38-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38d38-153">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="38d38-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38d38-154">輸入</span><span class="sxs-lookup"><span data-stu-id="38d38-154">INPUTS</span></span>

### <span data-ttu-id="38d38-155">所有</span><span class="sxs-lookup"><span data-stu-id="38d38-155">None</span></span>

## <span data-ttu-id="38d38-156">輸出</span><span class="sxs-lookup"><span data-stu-id="38d38-156">OUTPUTS</span></span>

### <span data-ttu-id="38d38-157">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="38d38-157">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="38d38-158">筆記</span><span class="sxs-lookup"><span data-stu-id="38d38-158">NOTES</span></span>

## <span data-ttu-id="38d38-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="38d38-159">RELATED LINKS</span></span>
