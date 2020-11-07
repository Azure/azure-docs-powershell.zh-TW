---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/resolve-azurermerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Resolve-AzureRmError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Resolve-AzureRmError.md
ms.openlocfilehash: 79c117ec7bf01c836c77fa6f6955481d7ba18a2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625461"
---
# <span data-ttu-id="5261c-101">Resolve-AzureRmError</span><span class="sxs-lookup"><span data-stu-id="5261c-101">Resolve-AzureRmError</span></span>

## <span data-ttu-id="5261c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5261c-102">SYNOPSIS</span></span>
<span data-ttu-id="5261c-103">顯示有關 PowerShell 錯誤的詳細資訊，以及有關 Azure PowerShell 錯誤的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="5261c-103">Display detailed information about PowerShell errors, with extended details for Azure PowerShell errors.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5261c-104">句法</span><span class="sxs-lookup"><span data-stu-id="5261c-104">SYNTAX</span></span>

### <span data-ttu-id="5261c-105">AnyErrorParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="5261c-105">AnyErrorParameterSet (Default)</span></span>
```
Resolve-AzureRmError [[-Error] <ErrorRecord[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5261c-106">LastErrorParameterSet</span><span class="sxs-lookup"><span data-stu-id="5261c-106">LastErrorParameterSet</span></span>
```
Resolve-AzureRmError [-Last] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5261c-107">說明</span><span class="sxs-lookup"><span data-stu-id="5261c-107">DESCRIPTION</span></span>
<span data-ttu-id="5261c-108">解析並顯示目前 PowerShell 會話中錯誤的詳細資訊，包括錯誤發生于腳本、堆疊追蹤以及所有內部和合計例外狀況的位置。</span><span class="sxs-lookup"><span data-stu-id="5261c-108">Resolves and displays detailed information about errors in the current PowerShell session, including where the error occurred in script, stack trace, and all inner and aggregate exceptions.</span></span> <span data-ttu-id="5261c-109">針對 Azure PowerShell 錯誤，提供調試服務問題的其他詳細資料，包括導致錯誤之要求和伺服器回應的完整詳細資料。</span><span class="sxs-lookup"><span data-stu-id="5261c-109">For Azure PowerShell errors provides additional detail in debugging service issues, including complete detail about the request and server response that caused the error.</span></span>

## <span data-ttu-id="5261c-110">示例</span><span class="sxs-lookup"><span data-stu-id="5261c-110">EXAMPLES</span></span>

### <span data-ttu-id="5261c-111">範例1：解決上一個錯誤</span><span class="sxs-lookup"><span data-stu-id="5261c-111">Example 1: Resolve the Last Error</span></span>
```
PS C:\> Resolve-AzureRmError -Last

   HistoryId: 3


Message        : Run Connect-AzureRmAccount to login.
StackTrace     :    at Microsoft.Azure.Commands.ResourceManager.Common.AzureRMCmdlet.get_DefaultContext() in AzureRmCmdlet.cs:line 85
                    at Microsoft.Azure.Commands.ResourceManager.Common.AzureRMCmdlet.LogCmdletStartInvocationInfo() in AzureRmCmdlet.cs:line 269
                    at Microsoft.WindowsAzure.Commands.Utilities.Common.AzurePSCmdlet.BeginProcessing() inAzurePSCmdlet.cs:line 299
                    at Microsoft.Azure.Commands.ResourceManager.Common.AzureRMCmdlet.BeginProcessing() in AzureRmCmdlet.cs:line 320
                    at Microsoft.Azure.Commands.Profile.GetAzureRMSubscriptionCommand.BeginProcessing() in GetAzureRMSubscription.cs:line 49
                    at System.Management.Automation.Cmdlet.DoBeginProcessing()
                    at System.Management.Automation.CommandProcessorBase.DoBegin()
Exception      : System.Management.Automation.PSInvalidOperationException
InvocationInfo : {Get-AzureRmSubscription}
Line           : Get-AzureRmSubscription
Position       : At line:1 char:1
                 + Get-AzureRmSubscription
                 + ~~~~~~~~~~~~~~~~~~~~~~~
HistoryId      : 3
```

<span data-ttu-id="5261c-112">取得最後一個錯誤的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="5261c-112">Get details of the last error.</span></span>

### <span data-ttu-id="5261c-113">範例2：解決會話中的所有錯誤</span><span class="sxs-lookup"><span data-stu-id="5261c-113">Example 2: Resolve all Errors in the Session</span></span>
```
PS C:\> Resolve-AzureRmError


   HistoryId: 8


RequestId      : b61309e8-09c9-4f0d-ba56-08a6b28c731d
Message        : Resource group 'contoso' could not be found.
ServerMessage  : ResourceGroupNotFound: Resource group 'contoso' could not be found.
                 (System.Collections.Generic.List`1[Microsoft.Rest.Azure.CloudError])
ServerResponse : {NotFound}
RequestMessage : {GET https://management.azure.com/subscriptions/00977cdb-163f-435f-9c32-39ec8ae61f4d/resourceGroups/co
                 ntoso/providers/Microsoft.Storage/storageAccounts/contoso?api-version=2016-12-01}
InvocationInfo : {Get-AzureRmStorageAccount}
Line           : Get-AzureRmStorageAccount -ResourceGroupName contoso -Name contoso
Position       : At line:1 char:1
                 + Get-AzureRmStorageAccount -ResourceGroupName contoso -Name contoso
                 + ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
StackTrace     :    at Microsoft.Azure.Management.Storage.StorageAccountsOperations.<GetPropertiesWithHttpMessagesAsync
                 >d__8.MoveNext()
                 --- End of stack trace from previous location where exception was thrown ---
                    at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
                    at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
                    at Microsoft.Azure.Management.Storage.StorageAccountsOperationsExtensions.<GetPropertiesAsync>d__7.
                 MoveNext()
                 --- End of stack trace from previous location where exception was thrown ---
                    at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
                    at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
                    at Microsoft.Azure.Management.Storage.StorageAccountsOperationsExtensions.GetProperties(IStorageAcc
                 ountsOperations operations, String resourceGroupName, String accountName)
                    at Microsoft.Azure.Commands.Management.Storage.GetAzureStorageAccountCommand.ExecuteCmdlet() in C:\
                 zd\azure-powershell\src\ResourceManager\Storage\Commands.Management.Storage\StorageAccount\GetAzureSto
                 rageAccount.cs:line 70
                    at Microsoft.WindowsAzure.Commands.Utilities.Common.AzurePSCmdlet.ProcessRecord() in
                 C:\zd\azure-powershell\src\Common\Commands.Common\AzurePSCmdlet.cs:line 642
HistoryId      : 8


   HistoryId: 5


Message        : Run Connect-AzureRmAccount to login.
StackTrace     :    at Microsoft.Azure.Commands.ResourceManager.Common.AzureRMCmdlet.get_DefaultContext() in C:\zd\azur
                 e-powershell\src\ResourceManager\Common\Commands.ResourceManager.Common\AzureRmCmdlet.cs:line 85
                    at Microsoft.Azure.Commands.ResourceManager.Common.AzureRMCmdlet.LogCmdletStartInvocationInfo() in
                 C:\zd\azure-powershell\src\ResourceManager\Common\Commands.ResourceManager.Common\AzureRmCmdlet.cs:lin
                 e 269
                    at Microsoft.WindowsAzure.Commands.Utilities.Common.AzurePSCmdlet.BeginProcessing() in
                 C:\zd\azure-powershell\src\Common\Commands.Common\AzurePSCmdlet.cs:line 299
                    at Microsoft.Azure.Commands.ResourceManager.Common.AzureRMCmdlet.BeginProcessing() in C:\zd\azure-p
                 owershell\src\ResourceManager\Common\Commands.ResourceManager.Common\AzureRmCmdlet.cs:line 320
                    at Microsoft.Azure.Commands.Profile.GetAzureRMSubscriptionCommand.BeginProcessing() in C:\zd\azure-
                 powershell\src\ResourceManager\Profile\Commands.Profile\Subscription\GetAzureRMSubscription.cs:line 49
                    at System.Management.Automation.Cmdlet.DoBeginProcessing()
                    at System.Management.Automation.CommandProcessorBase.DoBegin()
Exception      : System.Management.Automation.PSInvalidOperationException
InvocationInfo : {Get-AzureRmSubscription}
Line           : Get-AzureRmSubscription
Position       : At line:1 char:1
                 + Get-AzureRmSubscription
                 + ~~~~~~~~~~~~~~~~~~~~~~~
HistoryId      : 5
```

<span data-ttu-id="5261c-114">取得目前會話中發生之所有錯誤的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="5261c-114">Get details of all errors that have occurred in the current session.</span></span>

### <span data-ttu-id="5261c-115">範例3：解決特定的錯誤</span><span class="sxs-lookup"><span data-stu-id="5261c-115">Example 3: Resolve a Specific Error</span></span>
```
PS C:\> Resolve-AzureRmError $Error[0]


   HistoryId: 8


RequestId      : b61309e8-09c9-4f0d-ba56-08a6b28c731d
Message        : Resource group 'contoso' could not be found.
ServerMessage  : ResourceGroupNotFound: Resource group 'contoso' could not be found.
                 (System.Collections.Generic.List`1[Microsoft.Rest.Azure.CloudError])
ServerResponse : {NotFound}
RequestMessage : {GET https://management.azure.com/subscriptions/00977cdb-163f-435f-9c32-39ec8ae61f4d/resourceGroups/co
                 ntoso/providers/Microsoft.Storage/storageAccounts/contoso?api-version=2016-12-01}
InvocationInfo : {Get-AzureRmStorageAccount}
Line           : Get-AzureRmStorageAccount -ResourceGroupName contoso -Name contoso
Position       : At line:1 char:1
                 + Get-AzureRmStorageAccount -ResourceGroupName contoso -Name contoso
                 + ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
StackTrace     :    at Microsoft.Azure.Management.Storage.StorageAccountsOperations.<GetPropertiesWithHttpMessagesAsync
                 >d__8.MoveNext()
                 --- End of stack trace from previous location where exception was thrown ---
                    at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
                    at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
                    at Microsoft.Azure.Management.Storage.StorageAccountsOperationsExtensions.<GetPropertiesAsync>d__7.
                 MoveNext()
                 --- End of stack trace from previous location where exception was thrown ---
                    at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
                    at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
                    at Microsoft.Azure.Management.Storage.StorageAccountsOperationsExtensions.GetProperties(IStorageAcc
                 ountsOperations operations, String resourceGroupName, String accountName)
                    at Microsoft.Azure.Commands.Management.Storage.GetAzureStorageAccountCommand.ExecuteCmdlet() in C:\
                 zd\azure-powershell\src\ResourceManager\Storage\Commands.Management.Storage\StorageAccount\GetAzureSto
                 rageAccount.cs:line 70
                    at Microsoft.WindowsAzure.Commands.Utilities.Common.AzurePSCmdlet.ProcessRecord() in
                 C:\zd\azure-powershell\src\Common\Commands.Common\AzurePSCmdlet.cs:line 642
HistoryId      : 8
```

<span data-ttu-id="5261c-116">取得指定錯誤的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="5261c-116">Get details of the specified error.</span></span>

## <span data-ttu-id="5261c-117">參數</span><span class="sxs-lookup"><span data-stu-id="5261c-117">PARAMETERS</span></span>

### <span data-ttu-id="5261c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5261c-118">-DefaultProfile</span></span>
<span data-ttu-id="5261c-119">用於與 azure 進行通訊的認證、租使用者與訂閱</span><span class="sxs-lookup"><span data-stu-id="5261c-119">The credentials, tenant and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5261c-120">-錯誤</span><span class="sxs-lookup"><span data-stu-id="5261c-120">-Error</span></span>
<span data-ttu-id="5261c-121">一或多個要解決的錯誤記錄。</span><span class="sxs-lookup"><span data-stu-id="5261c-121">One or more error records to resolve.</span></span>  <span data-ttu-id="5261c-122">如果未指定任何參數，則會解析會話中的所有錯誤。</span><span class="sxs-lookup"><span data-stu-id="5261c-122">If no parameters are specified, all errors in the session are resolved.</span></span>

```yaml
Type: ErrorRecord[]
Parameter Sets: AnyErrorParameterSet
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5261c-123">-上次</span><span class="sxs-lookup"><span data-stu-id="5261c-123">-Last</span></span>
<span data-ttu-id="5261c-124">只解決會話中發生的最後一個錯誤。</span><span class="sxs-lookup"><span data-stu-id="5261c-124">Resolve only the last error that occurred in the session.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LastErrorParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5261c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5261c-125">CommonParameters</span></span>
<span data-ttu-id="5261c-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5261c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5261c-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5261c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5261c-128">輸入</span><span class="sxs-lookup"><span data-stu-id="5261c-128">INPUTS</span></span>

### <span data-ttu-id="5261c-129">ErrorRecord [] （系統管理）</span><span class="sxs-lookup"><span data-stu-id="5261c-129">System.Management.Automation.ErrorRecord[]</span></span>

## <span data-ttu-id="5261c-130">輸出</span><span class="sxs-lookup"><span data-stu-id="5261c-130">OUTPUTS</span></span>

### <span data-ttu-id="5261c-131">AzureErrorRecord 中的 Profile。</span><span class="sxs-lookup"><span data-stu-id="5261c-131">Microsoft.Azure.Commands.Profile.Errors.AzureErrorRecord</span></span>
<span data-ttu-id="5261c-132">有關 powershell 錯誤的資訊，不涉及 excpetion。</span><span class="sxs-lookup"><span data-stu-id="5261c-132">Information about a powershell error that does not involve an excpetion.</span></span>

### <span data-ttu-id="5261c-133">AzureExceptionRecord 中的 Profile。</span><span class="sxs-lookup"><span data-stu-id="5261c-133">Microsoft.Azure.Commands.Profile.Errors.AzureExceptionRecord</span></span>
<span data-ttu-id="5261c-134">錯誤的相關資訊，包括引發錯誤之例外狀況的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="5261c-134">Information about an error including detailed information on the exception that raised the error.</span></span>

### <span data-ttu-id="5261c-135">AzureRestExceptionRecord 中的 Profile。</span><span class="sxs-lookup"><span data-stu-id="5261c-135">Microsoft.Azure.Commands.Profile.Errors.AzureRestExceptionRecord</span></span>
<span data-ttu-id="5261c-136">Cleint/伺服器通訊中錯誤的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5261c-136">Information about errors in cleint/server communications.</span></span>  <span data-ttu-id="5261c-137">這通常會包含伺服器錯誤的重要資訊。</span><span class="sxs-lookup"><span data-stu-id="5261c-137">This will often contain important information about the error from the server.</span></span>

## <span data-ttu-id="5261c-138">筆記</span><span class="sxs-lookup"><span data-stu-id="5261c-138">NOTES</span></span>

## <span data-ttu-id="5261c-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="5261c-139">RELATED LINKS</span></span>

