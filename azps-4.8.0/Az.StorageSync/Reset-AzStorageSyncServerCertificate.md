---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/reset-Azstoragesyncservercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Reset-AzStorageSyncServerCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Reset-AzStorageSyncServerCertificate.md
ms.openlocfilehash: 41caebb8b43c7c050aef2dac77daf51eebdaf42a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129723"
---
# <span data-ttu-id="0714f-101">Reset-AzStorageSyncServerCertificate</span><span class="sxs-lookup"><span data-stu-id="0714f-101">Reset-AzStorageSyncServerCertificate</span></span>

## <span data-ttu-id="0714f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0714f-102">SYNOPSIS</span></span>
<span data-ttu-id="0714f-103">僅用於疑難排解。</span><span class="sxs-lookup"><span data-stu-id="0714f-103">Use for troubleshooting only.</span></span> <span data-ttu-id="0714f-104">這個命令會將用來描述伺服器身分識別的儲存同步處理伺服器憑證滾到儲存同步處理服務。</span><span class="sxs-lookup"><span data-stu-id="0714f-104">This command will roll the storage sync server certificate used to describe the server identity to the storage sync service.</span></span>

## <span data-ttu-id="0714f-105">句法</span><span class="sxs-lookup"><span data-stu-id="0714f-105">SYNTAX</span></span>

### <span data-ttu-id="0714f-106">StringParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="0714f-106">StringParameterSet (Default)</span></span>
```
Reset-AzStorageSyncServerCertificate [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0714f-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0714f-107">ObjectParameterSet</span></span>
```
Reset-AzStorageSyncServerCertificate [-ParentObject] <PSStorageSyncService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0714f-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="0714f-108">ParentStringParameterSet</span></span>
```
Reset-AzStorageSyncServerCertificate [-ParentResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0714f-109">說明</span><span class="sxs-lookup"><span data-stu-id="0714f-109">DESCRIPTION</span></span>
<span data-ttu-id="0714f-110">這個命令會將用來描述伺服器身分識別的儲存同步處理伺服器憑證滾到儲存同步處理服務。</span><span class="sxs-lookup"><span data-stu-id="0714f-110">This command will roll storage sync server certificate used to describe the server identity to the storage sync service.</span></span> <span data-ttu-id="0714f-111">這是用來在疑難排解案例中使用。</span><span class="sxs-lookup"><span data-stu-id="0714f-111">This is meant for to be used in troubleshooting scenarios.</span></span> <span data-ttu-id="0714f-112">當您呼叫此命令時，會取代伺服器憑證，更新此伺服器所註冊的儲存同步處理服務，只要提交金鑰的公用部分。</span><span class="sxs-lookup"><span data-stu-id="0714f-112">When calling this command, the server certificate is replaced, updating the storage sync service this server is registered with as well, by submitting the public part of the key.</span></span> <span data-ttu-id="0714f-113">由於產生新的憑證，此認證的到期時間也會更新。</span><span class="sxs-lookup"><span data-stu-id="0714f-113">Since a new certificate is generated, the expiration time of this cert is also updated.</span></span> <span data-ttu-id="0714f-114">您也可以使用這個命令來更新過期的憑證。</span><span class="sxs-lookup"><span data-stu-id="0714f-114">This command can also be used to update an expired certificate.</span></span> <span data-ttu-id="0714f-115">如果伺服器在長時間內處於離線狀態，可能會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="0714f-115">This can happen if a server is offline for an extended period of time.</span></span>

## <span data-ttu-id="0714f-116">示例</span><span class="sxs-lookup"><span data-stu-id="0714f-116">EXAMPLES</span></span>

### <span data-ttu-id="0714f-117">範例1</span><span class="sxs-lookup"><span data-stu-id="0714f-117">Example 1</span></span>
```powershell
PS C:\> Reset-AzStorageSyncServerCertificate -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="0714f-118">這個命令會以安全的方式將本機伺服器憑證匯總並告知伺服器新身分識別的對應儲存同步處理服務。</span><span class="sxs-lookup"><span data-stu-id="0714f-118">This command will roll the local server certificate and inform the corresponding storage sync service of the server's new identity, in a secure way.</span></span>

## <span data-ttu-id="0714f-119">參數</span><span class="sxs-lookup"><span data-stu-id="0714f-119">PARAMETERS</span></span>

### <span data-ttu-id="0714f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0714f-120">-DefaultProfile</span></span>
<span data-ttu-id="0714f-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0714f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0714f-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="0714f-122">-ParentObject</span></span>
<span data-ttu-id="0714f-123">StorageSyncService 物件，通常是透過參數傳遞。</span><span class="sxs-lookup"><span data-stu-id="0714f-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="0714f-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="0714f-124">-ParentResourceId</span></span>
<span data-ttu-id="0714f-125">StorageSyncService 父資源識別碼</span><span class="sxs-lookup"><span data-stu-id="0714f-125">StorageSyncService Parent Resource Id</span></span>

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

### <span data-ttu-id="0714f-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0714f-126">-PassThru</span></span>
<span data-ttu-id="0714f-127">在正常執行中，此 Cmdlet 在成功時不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="0714f-127">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="0714f-128">如果您提供 PassThru 參數，則在成功執行之後，Cmdlet 會將值寫入管道。</span><span class="sxs-lookup"><span data-stu-id="0714f-128">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="0714f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0714f-129">-ResourceGroupName</span></span>
<span data-ttu-id="0714f-130">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="0714f-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="0714f-131">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="0714f-131">-StorageSyncServiceName</span></span>
<span data-ttu-id="0714f-132">StorageSyncService 的名稱。</span><span class="sxs-lookup"><span data-stu-id="0714f-132">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="0714f-133">-確認</span><span class="sxs-lookup"><span data-stu-id="0714f-133">-Confirm</span></span>
<span data-ttu-id="0714f-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0714f-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0714f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0714f-135">-WhatIf</span></span>
<span data-ttu-id="0714f-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0714f-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0714f-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0714f-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0714f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0714f-138">CommonParameters</span></span>
<span data-ttu-id="0714f-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0714f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0714f-140">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0714f-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0714f-141">輸入</span><span class="sxs-lookup"><span data-stu-id="0714f-141">INPUTS</span></span>

### <span data-ttu-id="0714f-142">System.object</span><span class="sxs-lookup"><span data-stu-id="0714f-142">System.String</span></span>

### <span data-ttu-id="0714f-143">PSStorageSyncService 中的 StorageSync。</span><span class="sxs-lookup"><span data-stu-id="0714f-143">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="0714f-144">輸出</span><span class="sxs-lookup"><span data-stu-id="0714f-144">OUTPUTS</span></span>

### <span data-ttu-id="0714f-145">System.object</span><span class="sxs-lookup"><span data-stu-id="0714f-145">System.Object</span></span>
## <span data-ttu-id="0714f-146">筆記</span><span class="sxs-lookup"><span data-stu-id="0714f-146">NOTES</span></span>

## <span data-ttu-id="0714f-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="0714f-147">RELATED LINKS</span></span>