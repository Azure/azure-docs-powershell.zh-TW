---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: 7476E6DC-6DE6-4199-A680-5717053A8CC5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/remove-azurermservermanagementsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementSession.md
ms.openlocfilehash: b2ebde9e6cf0e94e43d41cd75ee7ee09674fc3ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453044"
---
# <span data-ttu-id="f6594-101">Remove-AzureRmServerManagementSession</span><span class="sxs-lookup"><span data-stu-id="f6594-101">Remove-AzureRmServerManagementSession</span></span>

## <span data-ttu-id="f6594-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f6594-102">SYNOPSIS</span></span>
<span data-ttu-id="f6594-103">移除伺服器管理會話。</span><span class="sxs-lookup"><span data-stu-id="f6594-103">Removes a Server Management session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6594-104">句法</span><span class="sxs-lookup"><span data-stu-id="f6594-104">SYNTAX</span></span>

### <span data-ttu-id="f6594-105">ByName</span><span class="sxs-lookup"><span data-stu-id="f6594-105">ByName</span></span>
```
Remove-AzureRmServerManagementSession [-ResourceGroupName] <String> [-NodeName] <String>
 [-SessionName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6594-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="f6594-106">ByObject</span></span>
```
Remove-AzureRmServerManagementSession [[-SessionName] <String>] [-Session] <Session>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6594-107">說明</span><span class="sxs-lookup"><span data-stu-id="f6594-107">DESCRIPTION</span></span>
<span data-ttu-id="f6594-108">**AzureRmServerManagementSession** Cmdlet 會移除 Azure Server 管理會話。</span><span class="sxs-lookup"><span data-stu-id="f6594-108">The **Remove-AzureRmServerManagementSession** cmdlet removes an Azure Server Management session.</span></span>

## <span data-ttu-id="f6594-109">示例</span><span class="sxs-lookup"><span data-stu-id="f6594-109">EXAMPLES</span></span>

## <span data-ttu-id="f6594-110">參數</span><span class="sxs-lookup"><span data-stu-id="f6594-110">PARAMETERS</span></span>

### <span data-ttu-id="f6594-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6594-111">-DefaultProfile</span></span>
<span data-ttu-id="f6594-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f6594-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6594-113">-NodeName</span><span class="sxs-lookup"><span data-stu-id="f6594-113">-NodeName</span></span>
<span data-ttu-id="f6594-114">指定此 Cmdlet 移除會話之節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="f6594-114">Specifies the name of the node on which this cmdlet removes the session.</span></span>

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

### <span data-ttu-id="f6594-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6594-115">-ResourceGroupName</span></span>
<span data-ttu-id="f6594-116">指定會話所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f6594-116">Specifies the name of the resource group that the session belongs to.</span></span>

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

### <span data-ttu-id="f6594-117">-會話</span><span class="sxs-lookup"><span data-stu-id="f6594-117">-Session</span></span>
<span data-ttu-id="f6594-118">指定此 Cmdlet 移除的會話。</span><span class="sxs-lookup"><span data-stu-id="f6594-118">Specifies the session that this cmdlet removes.</span></span>

<span data-ttu-id="f6594-119">您可以使用這個參數，而不是 *ResourceGroupName* 、 *NodeName* 和 *SessionName* 參數。</span><span class="sxs-lookup"><span data-stu-id="f6594-119">This parameter may be used instead of the *ResourceGroupName* , *NodeName* and *SessionName* parameters.</span></span>

```yaml
Type: Session
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6594-120">-SessionName</span><span class="sxs-lookup"><span data-stu-id="f6594-120">-SessionName</span></span>
<span data-ttu-id="f6594-121">指定此 Cmdlet 移除之會話的名稱。</span><span class="sxs-lookup"><span data-stu-id="f6594-121">Specifies the name of the session that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByObject
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6594-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6594-122">CommonParameters</span></span>
<span data-ttu-id="f6594-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f6594-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6594-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f6594-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6594-125">輸入</span><span class="sxs-lookup"><span data-stu-id="f6594-125">INPUTS</span></span>

### <span data-ttu-id="f6594-126">課時</span><span class="sxs-lookup"><span data-stu-id="f6594-126">Session</span></span>
<span data-ttu-id="f6594-127">參數 "Session" 接受管線中類型 "Session" 的值</span><span class="sxs-lookup"><span data-stu-id="f6594-127">Parameter 'Session' accepts value of type 'Session' from the pipeline</span></span>

## <span data-ttu-id="f6594-128">輸出</span><span class="sxs-lookup"><span data-stu-id="f6594-128">OUTPUTS</span></span>

## <span data-ttu-id="f6594-129">筆記</span><span class="sxs-lookup"><span data-stu-id="f6594-129">NOTES</span></span>

## <span data-ttu-id="f6594-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="f6594-130">RELATED LINKS</span></span>

[<span data-ttu-id="f6594-131">AzureRmServerManagementSession</span><span class="sxs-lookup"><span data-stu-id="f6594-131">Get-AzureRmServerManagementSession</span></span>](./Get-AzureRmServerManagementSession.md)

[<span data-ttu-id="f6594-132">新-AzureRmServerManagementSession</span><span class="sxs-lookup"><span data-stu-id="f6594-132">New-AzureRmServerManagementSession</span></span>](./New-AzureRmServerManagementSession.md)


