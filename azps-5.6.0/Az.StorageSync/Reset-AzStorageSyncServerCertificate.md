---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/reset-Azstoragesyncservercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Reset-AzStorageSyncServerCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Reset-AzStorageSyncServerCertificate.md
ms.openlocfilehash: 5d93249b6bb160d2659ead144d3fabda1af8438d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907425"
---
# <span data-ttu-id="11582-101">Reset-AzStorageSyncServerCertificate</span><span class="sxs-lookup"><span data-stu-id="11582-101">Reset-AzStorageSyncServerCertificate</span></span>

## <span data-ttu-id="11582-102">簡介</span><span class="sxs-lookup"><span data-stu-id="11582-102">SYNOPSIS</span></span>
<span data-ttu-id="11582-103">僅適用于疑難排解。</span><span class="sxs-lookup"><span data-stu-id="11582-103">Use for troubleshooting only.</span></span> <span data-ttu-id="11582-104">此命令會匯總儲存同步處理伺服器憑證，用來描述儲存空間同步處理服務的伺服器身分識別。</span><span class="sxs-lookup"><span data-stu-id="11582-104">This command will roll the storage sync server certificate used to describe the server identity to the storage sync service.</span></span>

## <span data-ttu-id="11582-105">語法</span><span class="sxs-lookup"><span data-stu-id="11582-105">SYNTAX</span></span>

### <span data-ttu-id="11582-106">StringParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="11582-106">StringParameterSet (Default)</span></span>
```
Reset-AzStorageSyncServerCertificate [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11582-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="11582-107">ObjectParameterSet</span></span>
```
Reset-AzStorageSyncServerCertificate [-ParentObject] <PSStorageSyncService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11582-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="11582-108">ParentStringParameterSet</span></span>
```
Reset-AzStorageSyncServerCertificate [-ParentResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11582-109">描述</span><span class="sxs-lookup"><span data-stu-id="11582-109">DESCRIPTION</span></span>
<span data-ttu-id="11582-110">此命令會匯總儲存同步處理伺服器憑證，用來描述儲存同步處理服務的伺服器身分識別。</span><span class="sxs-lookup"><span data-stu-id="11582-110">This command will roll storage sync server certificate used to describe the server identity to the storage sync service.</span></span> <span data-ttu-id="11582-111">這是用於疑難排解案例。</span><span class="sxs-lookup"><span data-stu-id="11582-111">This is meant for to be used in troubleshooting scenarios.</span></span> <span data-ttu-id="11582-112">呼叫此命令時，伺服器憑證會取代，同時提交金鑰的公用部分，以更新此伺服器所註冊的儲存空間同步處理服務。</span><span class="sxs-lookup"><span data-stu-id="11582-112">When calling this command, the server certificate is replaced, updating the storage sync service this server is registered with as well, by submitting the public part of the key.</span></span> <span data-ttu-id="11582-113">由於產生新憑證，因此也會更新此憑證的到期日。</span><span class="sxs-lookup"><span data-stu-id="11582-113">Since a new certificate is generated, the expiration time of this cert is also updated.</span></span> <span data-ttu-id="11582-114">此命令也可以用來更新過期的憑證。</span><span class="sxs-lookup"><span data-stu-id="11582-114">This command can also be used to update an expired certificate.</span></span> <span data-ttu-id="11582-115">如果伺服器處於離線狀態一段時間，就可能發生此情況。</span><span class="sxs-lookup"><span data-stu-id="11582-115">This can happen if a server is offline for an extended period of time.</span></span>

## <span data-ttu-id="11582-116">例子</span><span class="sxs-lookup"><span data-stu-id="11582-116">EXAMPLES</span></span>

### <span data-ttu-id="11582-117">範例 1</span><span class="sxs-lookup"><span data-stu-id="11582-117">Example 1</span></span>
```powershell
PS C:\> Reset-AzStorageSyncServerCertificate -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="11582-118">此命令會卷起本機伺服器憑證，並安全地通知對應的儲存同步處理服務伺服器的新身分識別。</span><span class="sxs-lookup"><span data-stu-id="11582-118">This command will roll the local server certificate and inform the corresponding storage sync service of the server's new identity, in a secure way.</span></span>

## <span data-ttu-id="11582-119">參數</span><span class="sxs-lookup"><span data-stu-id="11582-119">PARAMETERS</span></span>

### <span data-ttu-id="11582-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11582-120">-DefaultProfile</span></span>
<span data-ttu-id="11582-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="11582-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11582-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="11582-122">-ParentObject</span></span>
<span data-ttu-id="11582-123">StorageSyncService 物件，通常會通過參數。</span><span class="sxs-lookup"><span data-stu-id="11582-123">StorageSyncService Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService
Parameter Sets: ObjectParameterSet
Aliases: StorageSyncService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11582-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="11582-124">-ParentResourceId</span></span>
<span data-ttu-id="11582-125">StorageSyncService 父資源識別碼</span><span class="sxs-lookup"><span data-stu-id="11582-125">StorageSyncService Parent Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases: StorageSyncServiceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11582-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="11582-126">-PassThru</span></span>
<span data-ttu-id="11582-127">在一般執行中，此 Cmdlet 不會在成功時獲得任何值。</span><span class="sxs-lookup"><span data-stu-id="11582-127">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="11582-128">如果您提供 PassThru 參數，則成功執行之後，Cmdlet 會寫入值至管線。</span><span class="sxs-lookup"><span data-stu-id="11582-128">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="11582-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11582-129">-ResourceGroupName</span></span>
<span data-ttu-id="11582-130">資源組名。</span><span class="sxs-lookup"><span data-stu-id="11582-130">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11582-131">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="11582-131">-StorageSyncServiceName</span></span>
<span data-ttu-id="11582-132">StorageSyncService 的名稱。</span><span class="sxs-lookup"><span data-stu-id="11582-132">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11582-133">-確認</span><span class="sxs-lookup"><span data-stu-id="11582-133">-Confirm</span></span>
<span data-ttu-id="11582-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="11582-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11582-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11582-135">-WhatIf</span></span>
<span data-ttu-id="11582-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="11582-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="11582-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="11582-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11582-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11582-138">CommonParameters</span></span>
<span data-ttu-id="11582-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="11582-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11582-140">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="11582-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11582-141">輸入</span><span class="sxs-lookup"><span data-stu-id="11582-141">INPUTS</span></span>

### <span data-ttu-id="11582-142">System.String</span><span class="sxs-lookup"><span data-stu-id="11582-142">System.String</span></span>

### <span data-ttu-id="11582-143">Microsoft.Azure.Commands.StorageSync.models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="11582-143">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="11582-144">輸出</span><span class="sxs-lookup"><span data-stu-id="11582-144">OUTPUTS</span></span>

### <span data-ttu-id="11582-145">System.Object</span><span class="sxs-lookup"><span data-stu-id="11582-145">System.Object</span></span>
## <span data-ttu-id="11582-146">筆記</span><span class="sxs-lookup"><span data-stu-id="11582-146">NOTES</span></span>

## <span data-ttu-id="11582-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="11582-147">RELATED LINKS</span></span>
