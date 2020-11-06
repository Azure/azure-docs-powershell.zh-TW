---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: 1EA5F348-5EF4-4056-BA06-7B95E12E329D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/invoke-azurermservermanagementpowershellcommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Invoke-AzureRmServerManagementPowerShellCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Invoke-AzureRmServerManagementPowerShellCommand.md
ms.openlocfilehash: d4720a1159d55064a007a97df7233853200f1295
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447657"
---
# <span data-ttu-id="45a75-101">Invoke-AzureRmServerManagementPowerShellCommand</span><span class="sxs-lookup"><span data-stu-id="45a75-101">Invoke-AzureRmServerManagementPowerShellCommand</span></span>

## <span data-ttu-id="45a75-102">摘要</span><span class="sxs-lookup"><span data-stu-id="45a75-102">SYNOPSIS</span></span>
<span data-ttu-id="45a75-103">在節點上執行 Windows PowerShell 腳本區塊。</span><span class="sxs-lookup"><span data-stu-id="45a75-103">Executes a Windows PowerShell script block on a node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45a75-104">句法</span><span class="sxs-lookup"><span data-stu-id="45a75-104">SYNTAX</span></span>

### <span data-ttu-id="45a75-105">ByName</span><span class="sxs-lookup"><span data-stu-id="45a75-105">ByName</span></span>
```
Invoke-AzureRmServerManagementPowerShellCommand [-ResourceGroupName] <String> [-NodeName] <String>
 [-SessionName] <String> [-Command] <ScriptBlock> [-PowerShellSessionName <String>] [-RawOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45a75-106">BySession</span><span class="sxs-lookup"><span data-stu-id="45a75-106">BySession</span></span>
```
Invoke-AzureRmServerManagementPowerShellCommand [-Session] <Session> [-Command] <ScriptBlock>
 [-PowerShellSessionName <String>] [-RawOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45a75-107">說明</span><span class="sxs-lookup"><span data-stu-id="45a75-107">DESCRIPTION</span></span>
<span data-ttu-id="45a75-108">**AzureRmServerManagementPowerShellCommand** Cmdlet 會在由 Azure Server 管理閘道管理的節點上執行 Windows PowerShell 腳本區塊。</span><span class="sxs-lookup"><span data-stu-id="45a75-108">The **Invoke-AzureRmServerManagementPowerShellCommand** cmdlet executes a Windows PowerShell script block on a node managed by an Azure Server Management Gateway.</span></span>

## <span data-ttu-id="45a75-109">示例</span><span class="sxs-lookup"><span data-stu-id="45a75-109">EXAMPLES</span></span>

## <span data-ttu-id="45a75-110">參數</span><span class="sxs-lookup"><span data-stu-id="45a75-110">PARAMETERS</span></span>

### <span data-ttu-id="45a75-111">-Command</span><span class="sxs-lookup"><span data-stu-id="45a75-111">-Command</span></span>
<span data-ttu-id="45a75-112">指定要在目標節點上執行的腳本區塊。</span><span class="sxs-lookup"><span data-stu-id="45a75-112">Specifies the script block to run on the target node.</span></span>

```yaml
Type: ScriptBlock
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45a75-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45a75-113">-DefaultProfile</span></span>
<span data-ttu-id="45a75-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="45a75-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45a75-115">-NodeName</span><span class="sxs-lookup"><span data-stu-id="45a75-115">-NodeName</span></span>
<span data-ttu-id="45a75-116">指定要在其上執行腳本區塊之節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="45a75-116">Specifies the name of the node to run the script block on.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45a75-117">-PowerShellSessionName</span><span class="sxs-lookup"><span data-stu-id="45a75-117">-PowerShellSessionName</span></span>
<span data-ttu-id="45a75-118">指定目標節點上的 Windows PowerShell 運行空間名稱。</span><span class="sxs-lookup"><span data-stu-id="45a75-118">Specifies the name of the Windows PowerShell run space on the target node.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45a75-119">-RawOutput</span><span class="sxs-lookup"><span data-stu-id="45a75-119">-RawOutput</span></span>
<span data-ttu-id="45a75-120">指示 Cmdlet 會傳回包含節點輸出的完整物件。</span><span class="sxs-lookup"><span data-stu-id="45a75-120">Indicates that the cmdlet returns the complete object that contains the output from the node.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45a75-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45a75-121">-ResourceGroupName</span></span>
<span data-ttu-id="45a75-122">指定節點所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="45a75-122">Specifies the name of the resource group that the node belongs to.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45a75-123">-會話</span><span class="sxs-lookup"><span data-stu-id="45a75-123">-Session</span></span>
<span data-ttu-id="45a75-124">指定此 Cmdlet 用來連接至目標節點的 **會話** 物件。</span><span class="sxs-lookup"><span data-stu-id="45a75-124">Specifies the **Session** object that this cmdlet uses to connect to the target node.</span></span>

<span data-ttu-id="45a75-125">您可以指定此參數，而不是 *ResourceGroupName* 、 *NodeName* 、 *SessionName* 和 *PowerShellSessionName* 參數。</span><span class="sxs-lookup"><span data-stu-id="45a75-125">This parameter may be specified instead of the *ResourceGroupName* , *NodeName* , *SessionName* , and *PowerShellSessionName* parameters.</span></span>

```yaml
Type: Session
Parameter Sets: BySession
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="45a75-126">-SessionName</span><span class="sxs-lookup"><span data-stu-id="45a75-126">-SessionName</span></span>
<span data-ttu-id="45a75-127">指定要管理節點的會話名稱。</span><span class="sxs-lookup"><span data-stu-id="45a75-127">Specifies the name of the session to manage the node.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45a75-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45a75-128">CommonParameters</span></span>
<span data-ttu-id="45a75-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="45a75-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45a75-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="45a75-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45a75-131">輸入</span><span class="sxs-lookup"><span data-stu-id="45a75-131">INPUTS</span></span>

### <span data-ttu-id="45a75-132">課時</span><span class="sxs-lookup"><span data-stu-id="45a75-132">Session</span></span>
<span data-ttu-id="45a75-133">參數 "Session" 接受管線中類型 "Session" 的值</span><span class="sxs-lookup"><span data-stu-id="45a75-133">Parameter 'Session' accepts value of type 'Session' from the pipeline</span></span>

## <span data-ttu-id="45a75-134">輸出</span><span class="sxs-lookup"><span data-stu-id="45a75-134">OUTPUTS</span></span>

### <span data-ttu-id="45a75-135">System.object</span><span class="sxs-lookup"><span data-stu-id="45a75-135">System.Object</span></span>

## <span data-ttu-id="45a75-136">筆記</span><span class="sxs-lookup"><span data-stu-id="45a75-136">NOTES</span></span>

## <span data-ttu-id="45a75-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="45a75-137">RELATED LINKS</span></span>

[<span data-ttu-id="45a75-138">Azure Server 管理 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="45a75-138">Azure Server Management Cmdlets</span></span>](./AzureRM.ServerManagement.md)


